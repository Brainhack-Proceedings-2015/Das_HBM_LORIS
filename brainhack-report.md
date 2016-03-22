---
event: '2015 OHBM Hackathon (HI)'

title:  'LORIS: DICOM Anonymizer'

author:

- initials: SD
  surname: Das
  firstname: Samir
  email: samir@acelab.mcgill.edu.ca
  affiliation: aff1
  corref: aff1
- initials: CM
  surname: Madjar
  firstname: C.
  email: cecile.madjar@gmail.com
  affiliation: aff2
- initials: AS
  surname: Sengupta
  firstname: A.
  email: somename@someplace.edu
  affiliation: aff3
- initials: ZM
  surname: Mohades
  firstname: Z.
  email: somename@someplace.edu
  affiliation: aff1

affiliations: 

- id: aff1
  orgname: 'Montréal Neurological Institute, McGill University and Institute of Pscychology'
  street: 1 Queen St
  postcode: 055332
  city: Montréal
  state: Québec
  country: Canada
- id: aff2
  orgname: 'Douglas Mental Health Institute'
  street: 2 Queen St
  postcode: 87777
  city: Montréal
  state: Québec
  country: Canada
- id: aff3
  orgname: 'Otto-von-Guericke University'
  street: Otto-von-Guericke Strasse 3B
  postcode: 87777
  city: Magdeburg
  state: 
  country: Germany

url: http://github.com/DICOM_anonymizer

coi: None

acknow: The authors would like to thank the organizers and attendees of the 2015 OHBM Hackathon.

contrib: SD, CM, AS, and ZM wrote the software and the report.
  
bibliography: brainhack-report

gigascience-ref: REFXXX
...

#Introduction
The purpose of this Brainhack project was to create a simple application, with the least dependencies, for anonymization of DICOM files directly on a workstation. 

Anonymization of DICOM datasets is a requirement before an imaging study can be uploaded in a web-based database system, such as LORIS\cite{Das2011}. Currently, a simple and efficient interface for the anonymization of such imaging datasets, which works on all operating systems and is very light in terms of dependencies, is not available.

#Approach
Here, we created a DICOM anonymizer that is a simple graphical tool that uses [PyDICOM](https://github.com/darcymason/pydicom) package to anonymize DICOM datasets easily on any operating system, with no dependencies except for the default Python and NumPy packages. DICOM anonymizer is available for all UNIX systems (including Mac OS) and can be easily installed on Windows computers as well (see [PyDICOM installation](http://pydicom.readthedocs.org/en/latest/getting_started.html)). The GUI (using [tkinter](https://wiki.python.org/moin/TkInter)) and the processing pipeline were designed in Python. Executing the anonymizer_gui.py script with a python compiler will start the program. Figure 1 illustrates how to use the program to anonymize a DICOM study.

\begin{figure}[h!]
  \includegraphics[width=.47\textwidth]{loris_screenshot.png}
  \caption{\label{centfig} How to use the DICOM anonymizer step by step.}
\end{figure}


#Results
This graphical tool, designed to be easy-to-use, platform independent and have minimum dependencies, produces two zip files. One zip file includes the original DICOM files and the other contains the anonymized DICOM outputs. 


# Conclusions
The DICOM anonymizer is a simple standalone graphical tool that facilitates anonymization of DICOM datasets on any operating system. These anonymized studies can be uploaded to a web-based database system, such as LORIS, without compromising the patient or participant’s identity.

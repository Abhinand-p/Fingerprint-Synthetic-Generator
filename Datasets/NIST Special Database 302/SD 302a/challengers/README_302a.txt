NIST SPECIAL DATABASE 302a
==========================

ABOUT
-----
NIST Special Database (SD) 302 is a collection of biometric data collected at
the Intelligence Advanced Research Project Activity's Nail to Nail (N2N)
Fingerprint Challenge. SD 302a specifically consists of the friction ridge
imagery in Portable Network Graphics (PNG) format from the Challenger finalists.
For complete details, please refer to NIST Technical Note 2007 [1]. For details
about the N2N Fingerprint Challenge itself, please refer to NIST Interagency
Report 8210 [2].

ERRATA
------
For a growing list of known errata in this version of the dataset, please visit:
https://www.nist.gov/document/erratasd302txt

DIRECTORY STRUCTURE
-------------------
The directory structure of SD 302a is as follows:

images
├── ...
└── challengers                            # Collection type
    ├── A                                  # Challenger device code
    │   └── roll                           # Impression type
    │       ├── checksum_A_roll_png.csv    # File checksums
    │       └── png                        # Image format
    │           ├── 00002303_A_roll_01.png
    │           ├── 00002303_A_roll_02.png
    │           ├── 00002303_A_roll_03.png
    │           └── ...
    └── ...

This directory structure was chosen to allow for NIST to easily deliver future
versions of the same images in different file formats, as well as images from
other modalities and device types alongside this distribution.

The topmost `images` directory contains a directory for each of the collection
types, from the N2N Fingerprint Challenge, limited to `challengers` in SD 302a.
The directories under `challengers` are named after the Challenger whose device
was used. Inside each Challenger device directory are nested options for the
data formats within.

For SD 302a, challenger data is rolled impression PNG files. These are the
images that were returned from N2N Fingerprint Challenger devices. As such, the
resolution varies between the devices, but is encoded within the PNG's file
header.

Images files are contained in the deepest directory and are named in the form
SUBJECT_DEVICE_CAPTURE_FRGP.EXT, where:
   SUBJECT: Unique identifier for this study participant.
    DEVICE: The short code used to refer to the device.
   CAPTURE: The capture type characterized by the image. For SD 302a, all
            captures were defined to be "roll."
      FRGP: The ANSI/NIST-ITL 1-2011 Update:2015 friction ridge generalized
            position code.
       EXT: File format extension.

A comma-separated value (CSV) file, `checksum_DEVICE_CAPTURE_EXT.csv`,
accompanies every directory of images. Contained in this file are the SHA 256
checksums of the files contained within the named directory.

ACKNOWLEDGMENTS
---------------
A data collection of the size and scale presented at the N2N Fingerprint
Challenge required the coordination and cooperation of dozens of individuals,
without whom the Challenge would not have been possible.

Thank you to IARPA for sponsoring the N2N Fingerprint Challenge and supporting
advancements in fingerprint capture and recognition.

Thank you to Rebecca Allegar, Nathaniel Short, and the many members of the Booz
Allen Hamilton (BAH) team that helped IARPA create, organize, plan, and
successfully execute the N2N Fingerprint Challenge.

Thank you to Ellen Fuller, Christopher Nardone, and the rest of the Johns
Hopkins University Applied Physics Laboratory (JHU APL) team for graciously
hosting the N2N Fingerprint Challenge and providing the infrastructure by which
N2N Challengers submitted imagery.

Thank you to the many JHU APL, BAH, IARPA, NIST, and Schwarz Forensic
Enterprises (SFE) employees who spent countless hours digitizing and isolating
latents.

Thank you to Crossmatch and IDEMIA for providing high-resolution palm scanners
for the week of the N2N Fingerprint Challenge in order to help capture exemplar
palm data for distribution with the Challenge latent print dataset.

Thank you to the Biometrics Research Group at Michigan State University for
providing a prototype open source single finger capture device for auxiliary
data collection.

Thank you to the staff of the Department of Homeland Security (DHS) Maryland
Test Facility for their assistance in prototyping the Challenge data collection.

LICENSE
-------
Users of SD 302 shall adhere to all terms agreed to upon obtaining SD 302.

DISCLAIMER
----------
Certain commercial equipment, instruments, or materials are identified in this
document in order to specify the development procedure adequately. Such
identification is not intended to imply recommendation or endorsement by the
National Institute of Standards and Technology, nor is it intended to imply
that the materials or equipment identified are necessarily the best available
for the purpose.

[1] Fiumara G, Flanagan P, Grantham J, Ko K, Marshall K, Schwarz M, Tabassi E,
    Woodgate B, Boehnen C (2019) NIST Special Database 302: Nail to Nail
    Fingerprint Challenge. NIST Technical Note 2007.
    https://doi.org/10.6028/NIST.TN.2007

[2] Fiumara G, Tabassi E, Flanagan P, Grantham J, Ko K, Marshall K, Schwarz M,
    Woodgate B, Boehnen C (2018) Nail to Nail Fingerprint Challenge: Prize
    Analysis. NIST Interagency Report 8210. https://doi.org/10.6028/NIST.IR.8210

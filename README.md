Script : calibspect.py
Description : Add DICOM tags to allow PET-like quantification in NM DICOM files.
Author : Arnaud Dieudonné
Date : 28/03/2025
Version : 1.0

Usage :
    python calibspect.py -i <input_folder> -s <sensitivity> -n <number_of_detectors> -a <activity> -d <injection_date> [-sim]

Arguments :
    -i : Directory containing the NM DICOM files to process (required).
    -s : Sensitivity in counts/s/MBq (optional).
    -n : Number of detectors (optional, default = 1).
    -a : Injected activity in MBq (optional).
    -d : Injection date in YYYYMMDDHHMMSS format (optional).
    -sim : Simulation mode (no modifications are written to the files).

Example :
    python calibspect.py -i ./dicom_files -s 0.5 -n 2 -a 150 -d 20250101083000

The number of detectors (-n) should be set depending on the value of sensitivity provided through the -s argument.
If the sensitivity is provided for the system, i.e. all detector heads, then the number of detectors should be set to 1 (-n 1).
If the sensitivity is provided for one detector head (average sensitivity), then the number of detectors should be set to the actual number of detector heads in the system, which is usually 2 (-n 2).

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

# Invoice-Text-Extraction
File and Folder Information

# run.py 
Python script that give back all the recognized information from an image or invoice.
         
    Syntax: python run.py --modelDir "models/FOLDER" --fileType "img (for image file) or txt(for text file)" --file "path of img or text file"
    example: python run.py --modelDir models/AIDL_NER_DO-0.30_EP-20_80_PERC_DATA --fileType img --file sample.jpg
             python run.py --modelDir models/AIDL_NER_DO-0.30_EP-20_80_PERC_DATA --fileType txt --file sample.txt
         
# model
Folder that contains all the Spacy Models

     AIDL_NER_DO-0.30_EP-20_80_PERC_DATA : Dropout-0.3, Epochs-20, trained on 80% of the Data
     AIDL_NER_DO-0.30_EP-20_90_PERC_DATA : Dropout-0.3, Epochs-20, trained on 90% of the Data
     AIDL_NER_DO-0.30_EP-20_100_PERC_DATA : Dropout-0.3, Epochs-20, trained on 100% of the Data
     
# requirements.txt
File that has all the dependencies needed in order to run this program

# Installation
         virtualenv --python "path to Python3 64bit" aidl2020-team-ace
         cd aidl2020-team-ace
         Scripts\activate
         pip install -r requirements.txt
         python run.py --modelDir models/AIDL_NER_DO-0.30_EP-20_80_PERC_DATA --fileType img --file sample.jpg
         
         #### Output ####
         {
           "Date": "29-11-2019",
           "Invoice number": "201911291623",
           "Items": [
             "YOU ARE THE GREATE\nST MUG-FATHER",
             "PRINTED PAPER MATT\nER\nCRAFT PAPER BAG- H"
           ],
           "Store address": "PHOENIX MARKETCITY\n",
           "Store address-2": "S-23,IIND FLOOR, 142, VELACHERY MAIN ROAD,\nCHENNAI-600042",
           "Store name": "ARCHIES",
           "Store name-1": "ARCHIES",
           "Time": "16:22",
           "Total bill amount": 434.0
         }

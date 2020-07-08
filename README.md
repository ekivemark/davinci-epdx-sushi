# davinci-epdx-sushi

This is the Hl7 Da Vinci Payer Data Exchange (PDex) Implementation Guide (IG) converted from Trifolia-FHIR to FHIR Shorthand and Sushi.

To use sushi you should follow the install instructions here:

https://build.fhir.org/ig/HL7/fhir-shorthand/sushi.html#configuration-file
    
This requires the installation of Node.js and npm.

Once installed you should switch to the fishtank directory.

To compile and run the IG:

    cd fishtank
    sushi .
    cd build
    ./_updatePublisher.sh
    ./_genonce.sh 

    
The config.yaml file in the fishtank directory controls the configuration of the Implementation Guide.

The table of contents in the IG is controlled in the Pages section of config.yaml.

To see the output of the IG in a browser:

    {base directory}/fishtank/build/output/index.html
    
file:///./fishtank/build/output/index.html


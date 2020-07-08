# davinci-epdx-sushi

This is the Hl7 Da Vinvi Payer Data Exchange Implementation Guide converted from Trifolia-Fhir to Fhir Shorthand and Sushi.

To use sushi you should follow the install instructions here:

https://build.fhir.org/ig/HL7/fhir-shorthand/sushi.html#configuration-file
    
This requires the installation of Node.js and npm.

once installed you should switch to the fishtank directory.

Then run:

    sushi .
    cd build
    ./_updatePublisher.sh
    ./_genonce.sh 

    
The config.yaml file in the fishtank directory controls the configuration of the Implementation Guide.

The table of contents in the IG is controlled in the Pages section of config.yaml.



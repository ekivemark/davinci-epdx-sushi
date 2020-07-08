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
    
file:///{base directory}/fishtank/build/output/index.html

When you are satisfied with the build of the IG you can copy the output from the the build directory:

    ig.ini
    generated_output/*
    input/*
    input-cache/*
    output/*
    temp/*
    template/*
    
Copy the files to the davinci-epdx repository that is used to supply build.fhir.org.

Once the files are copied to davinci-epdx do:

    git status
    
Use git add and git rm commands to update a commit.

Then issue a commit and push command:

    git commit -am "my commit message"
    git push origin master

Once committed to the master branch a build should be triggered on build.fhir.org.

Once the IG has successfully been built on build.fhir.org you can view it via the Browser:

http://build.fhir.org/ig/HL7/davinci-epdx/index.html

     

Back to [Projects List](../../README.md#ProjectsList)

# Slicer On Demand

## Key Investigators

- Steve Pieper (Isomics, Inc. Cambridge MA, USA)
- Curt Lisle (Knowledgevis, Maitland, Florida, USA)
- Andrey Fedorov (BWH, Boston, MA, USA)

# Project Description

The goal is to allow people to quickly transition from viewing images to doing more complex tasks such as segmentation or registration.

## Objective

<!-- Describe here WHAT you would like to achieve (what you will have as end result). -->

1. A quick and easy way to get a functioning Slicer environment
2. Ability to browse data, e.g. in IDC, and load same data in cloud-hosted Slicer
3. Pass login credentials from web to Slicer to allow load/save of confidential data

## Approach and Plan

<!-- Describe here HOW you would like to achieve the objectives stated above. -->

1. Build on existing [SlicerMachines GCP boot images](https://github.com/pieper/SlicerMachines)
1. Prototype using [the IDC sandbox](https://idc-sandbox-000.web.app/) that already supports login
1. Use [GCP JavaScript API](https://cloud.google.com/compute/docs/tutorials/javascript-guide) to launch and monitor jobs

## Progress and Next Steps

<!-- Update this section as you make progress, describing of what you have ACTUALLY DONE. If there are specific steps that you could not complete then you can describe them here, too. -->

1. Steve successfulluy tested creation of a VM automatically using the Google API and launched a Slier Docker container inside the VM
3. We met and discussed methods for encrypting traffic to the "pop up" Slicer-in-the-cloud using Google Cloud infrastructure options.
4. A use case was identified where an IDC cohort manifest could be passed to the Slicer VM and the cohort could be automatically loaded for the user.
5. We had a discussion with Kitware regarding the composition of the Slicer Docker containers: It would be nice to consolidate dockerfile of general use into https://github.com/Slicer/SlicerDocker
6. Next Steps: continue testing ssl protection and how to control access to the newly booted Slicer instance, as it shouldn't be publically accessible.

# Illustrations

<!-- Add pictures and links to videos that demonstrate what has been accomplished.
![Description of picture](Example2.jpg)
![Some more images](Example2.jpg)
-->

# Background and References
* [Review of Cloud efforts from last virtual Project Week](https://projectweek.na-mic.org/PW34_2020_Virtual/Projects/Slicer_in_Cloud_Environments/).
* [Prelimary work from last in-person Project Week](https://projectweek.na-mic.org/PW33_2020_GranCanaria/Projects/OHIFSlicerBridge/)

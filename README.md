
# Fingerprint Synthetic Generator

This repository provides various implementations for generating synthetic fingerprints using different machine learning models, including GANs, conditional and unconditional diffusion models. The aim is to generate realistic and diverse fingerprint impressions for research and practical applications.

## Introduction

This project develops a framework for generating synthetic fingerprints using various machine learning models. The generated fingerprints can be used for testing, research, and enhancing the security of biometric systems.

## FPGAN-Control Based Implementation

[FPGAN-Control based implementation](FPGAN-Control%20based%20implementation) implements the Fingerprint Generation using FPGAN with controlled parameters. It allows users to generate fingerprints with specific attributes such as fingerprint type, acquisition device, and pressure level.

![Total.gif](FPGAN-Control%20based%20implementation%2FVisualizing_Generated_Images%2FTotal.gif)

## GAN Based Implementation

[GAN based implementation](GAN%20based%20implementation) focuses on generating fingerprints using Generative Adversarial Networks. This model is designed to produce realistic fingerprint images with variability.

![generated_images_animation_NIST_Special_Dataset.gif](GAN%20based%20implementation%2Fgenerated_images_animation_NIST_Special_Dataset.gif)
![generated_images_animation_Sokoto_Coventry_Fingerprint_Dataset.gif](GAN%20based%20implementation%2Fgenerated_images_animation_Sokoto_Coventry_Fingerprint_Dataset.gif)

## Conditional Diffusion Model

[conditional_diffusion_model](conditional_diffusion_model) generates fingerprints based on specific conditions or inputs. This model uses advanced diffusion processes to create high-quality fingerprints.

## Unconditional Diffusion Model

[unconditional_diffusion_model](unconditional_diffusion_model)does not require specific conditions or inputs to generate fingerprints. It utilizes a generalized approach to create diverse fingerprint patterns.

## Validation Techniques

Validation techniques are crucial for ensuring the generated fingerprints' quality and diversity. [Validation Techniques](Validation%20Techniques) provides various methods and metrics to validate synthetic fingerprints.

## Usage

To use the models provided in this repository, follow the instructions in each respective folder. The repository includes detailed setup instructions, scripts, and examples for each implementation.

## Results

Sample results and comparisons for each model are included in their respective folders. Check the generated samples to evaluate the models' performance.
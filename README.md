[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/ol4GAg0d)
[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=15423626)
<!--
Name of your teams' final project
-->
# Application of Autoencoders in Earthquake Engineering

## [National Action Council for Minorities in Engineering(NACME)](https://www.nacme.org) Artificial Intelligence - Machine Learning (AIML) Intensive Summer Bootcamp at the [University of Southern California](https://viterbischool.usc.edu)

## Sponsors

|Apple|NACME|University of Southern California|
|-----|-----|---|
|<img width="409" alt="Screenshot 2024-08-01 at 10 03 54 AM" src="https://github.com/user-attachments/assets/e5226e1e-de2b-441b-8ff5-4c96a0f8d9f0">|![nacme_logo_blue_green(vector)](https://github.com/user-attachments/assets/dedf3290-fe9f-4b06-b279-4711788f8a0e)|![USC logo](https://github.com/user-attachments/assets/0a6489b2-ca3f-4157-9a98-a5cc06b5e130)|




Developed by: 
- [Darryn Dunn](https://github.com/GreeksGods) - `Computer Science: Concentration in Video Game Development` - `University of the Pacific (UOP)`
- [Eliska Peacock](https://github.com/eliskuh) - `Symbolic Systems: Concentration in Media & Communication` - `Stanford University` 
- [Johnny Williams](https://github.com/BlackMoonCoder) - `Computer Science: Concentration in Software Engineering` - `Louisiana State University (LSU)` 

## Description
<!--
Could you briefly describe what your project is doing and what tools are used? In addition, you can drop screenshots directly into your README file to add them to your README. Could you take these from your presentations?
-->
This project, led by Professor Chukwuebuka Nweke, focuses on estimating and predicting ground shaking intensity for earthquake engineering. The core of this research involves analyzing [microtremor data collected from a site in Utah](https://drive.google.com/drive/folders/16O1wZpk-KWNdID4VLngiQLZLDRB7E2hB?usp=share_link) in order to gain a deeper understanding of the complex interactions between seismic waves and subsurface structures.
The project involves identifying both observed and latent features from the horizontal-to-vertical spectral ratio (HVSR) curves. By mapping these features against one another, the research seeks to detail the relationship between subsurface geologic structures and seismic waves.
The project utilizes autoencoders to help identify latent features that may contribute to understanding of seismic responses. The insights gained from this research could lead to more accurate seismic hazard assessments and better-informed earthquake engineering practices. By leveraging advanced data analysis techniques, it aims to enhance our ability to predict ground shaking intensity and improve the safety and resilience of structures in earthquake-prone areas.


## Presentations

[Slideshow](https://docs.google.com/presentation/d/11Zdzf-rf7Cmzk8GiqWX2ohVi4NAAmndL2K1t2xU4m2w/edit?usp=sharing)

Poster:
[Earthquake Group Poster Presentation (4).pdf](https://github.com/user-attachments/files/16447678/Earthquake.Group.Poster.Presentation.4.pdf)

## The Data
We are using a dataset provided by graduate students working on their PhD thesis. The data, collected in Utah, is organized into 3-hour segments, each containing an embedded 3-minute segment for frequency comparison.

<img width="612" alt="Screenshot 2024-08-01 at 9 04 03 AM" src="https://github.com/user-attachments/assets/fdd829a3-92a0-4c1d-9797-08dad1448ed6">

To help us visualize the data initially, we plotted each 3-minute interval against the frequency for one three-hour segment. This provided a clear visual representation, allowing us to compare future data to ensure it resembles the original raw data.

<img width="612" alt="Screenshot 2024-08-01 at 9 04 11 AM" src="https://github.com/user-attachments/assets/08c14a5e-a37d-413c-962e-613ff0f43af8">

## The Autoencoder

An autoencoder consists of two main parts: an encoder and a decoder. The encoder compresses the input into a latent space representation, while the decoder reconstructs the original input from this compact representation.

<img width="430" alt="Screenshot 2024-08-01 at 9 05 00 AM" src="https://github.com/user-attachments/assets/62f2af9b-9180-4d12-a4ea-398fbff15880">

## Seen Features

Before plotting the output of the autoencoder, we needed to visualize all the observed features. These features included the area under the curve, peak amplitudes, peak frequencies, and other relevant metrics. By plotting these features, we could gain a comprehensive understanding of the data's characteristics. The following graph illustrates the peak amplitude, area under the curve, and peak frequencies, providing a detailed view of the key features we analyzed.

<img width="822" alt="Screenshot 2024-08-01 at 9 04 26 AM" src="https://github.com/user-attachments/assets/02bbbe97-2bbb-423c-85e3-3ddaeeb7fd4d">

Examining the area under the curve made it challenging to pinpoint the exact times, as the details were not immediately clear. To address this, we created a separate, more focused graph specifically to highlight the area under the curve. This additional visualization enhances our understanding by providing a clearer, more detailed view of the time intervals, ensuring we can accurately interpret the data.

<img width="685" alt="Screenshot 2024-08-01 at 9 04 37 AM" src="https://github.com/user-attachments/assets/8ac02118-ddc2-44f3-bb37-fc8eccb908ec">

After plotting the area under the curve for a single three-hour interval, we realized that this approach might not capture the overall trends effectively. Therefore, we decided it would be more informative to calculate and represent the average area under the curve across all eight three-hour intervals we had. This approach allows us to gain a clearer understanding of the data's overall patterns and trends, facilitating better analysis and comparison.

<img width="440" alt="Screenshot 2024-08-01 at 9 04 49 AM" src="https://github.com/user-attachments/assets/0838db9a-c852-4ed0-a415-4c8137c3ca33">

## Unseen Features

This graph represents the unseen features generated by the autoencoder. In this visualization, we are plotting one three-hour interval against three different latency features, providing insights into the output produced by the model. By analyzing these relationships, we can better understand how the autoencoder captures and represents the underlying patterns in the data. This comparative analysis allows us to assess the model's performance and explore how effectively it retains important information from the original dataset.

<img width="841" alt="Screenshot 2024-08-01 at 9 50 12 AM" src="https://github.com/user-attachments/assets/847a368d-1d56-4bf3-8688-e85cdfc23eb6">

Now that we have visualized the features plotted against themselves, we can take the analysis a step further by plotting these unseen features against various observed features, including the area under the curve, peak amplitude, and peak frequency. This approach allows us to explore the relationships between the latent representations generated by the autoencoder and the known features in our dataset. By examining these correlations, we can gain deeper insights into how the autoencoder captures essential patterns in the data, facilitating a better understanding of the underlying dynamics and helping us validate the model's effectiveness.

<img width="409" alt="Screenshot 2024-08-01 at 9 50 37 AM" src="https://github.com/user-attachments/assets/7491e883-5189-434b-b798-7f61d7609f76">
<img width="409" alt="Screenshot 2024-08-01 at 9 52 44 AM" src="https://github.com/user-attachments/assets/ac82fae4-7805-40ae-8a9d-79048b139751">
<img width="409" alt="Screenshot 2024-08-01 at 9 52 48 AM" src="https://github.com/user-attachments/assets/5992a737-dd8a-4587-adc0-b97e098680ef">

## Questions

Please feel free to contact us

Darryn Dunn: d_dunn5@u.pacific.edu

Eliska Peacock: eliska@stanford.edu

Johnny Williams: Jwil854@lsu.edu

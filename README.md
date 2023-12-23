# Geospatial Analysis and Remote Sensing for Water Quality Assessment

## Overview

This project employs geospatial analysis and remote sensing techniques to assess water quality in a specific geographical location. Leveraging satellite imagery and scientific algorithms, the script extracts GPS information from the provided image, retrieves relevant satellite data using Google Earth Engine, and calculates essential indices such as the Normalized Difference Vegetation Index (NDVI) and the Normalized Difference Water Index (NDWI). The results contribute to a comprehensive evaluation of vegetation health and water quality parameters.

## Prerequisites

- Python 3.x
- Required Python packages: `requests`, `json`, `Pillow`, `folium`, `earthengine-api`

## Scientific Methodology

### 1. GPS Information Extraction

The script utilizes Exif data from the image, extracting geotags such as GPSLatitude and GPSLongitude, crucial for pinpointing the image's location on Earth's surface.

### 2. Satellite Data Retrieval

Google Earth Engine is employed to access Sentinel-2 satellite imagery. The script filters images based on geographical bounds, temporal criteria, and cloud coverage, ensuring the selection of high-quality data for analysis.

### 3. Vegetation Health Assessment (NDVI)

The NDVI is calculated using near-infrared and red spectral bands from the satellite imagery. This index provides insights into the health and density of vegetation in the specified area.

### 4. Water Quality Parameters

Key bands from the Sentinel-2 imagery are selected to derive water quality parameters. These include bands related to the blue, green, and near-infrared spectra, offering valuable information about water characteristics.

### 5. Normalized Difference Water Index (NDWI)

The NDWI is computed to quantify the presence of water in the designated location. It is particularly useful for discriminating between water bodies and other land features.

### 6. Qualitative Water Quality Assessment

Based on the NDWI value, the script categorizes water quality into "good," "moderate," or "poor," providing a qualitative assessment of the environmental conditions.

## Usage

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/your-repository.git
    ```

2. Install the required Python packages:

    ```bash
    pip install requests json Pillow folium earthengine-api
    ```

3. Obtain a Google Earth Engine API key: [Google Earth Engine](https://earthengine.google.com/)

4. Update the script with your Google Earth Engine API key:

    ```python
    # Set up Earth Engine
    ee.Initialize(
        credential_key='your_earth_engine_api_key'
    )
    ```

5. Replace 'your_image_path' in the script with the actual path to your image:

    ```python
    image_path = 'path/to/your/image.jpg'
    ``

6. Run the script:

    ```bash
    python script_name.py
    ```

## Conclusion

This project provides a robust methodology for assessing water quality using advanced geospatial techniques. The combination of satellite imagery, scientific indices, and qualitative assessments contributes to a comprehensive understanding of environmental conditions in the specified location.

---

Feel free to tailor the README further to reflect the specific scientific context, methodologies, and objectives of your water quality assessment project.

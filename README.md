# The Geolocation Radar
<p align="left">
  <img src="https://github.com/user-attachments/assets/6ffc6bc3-a894-4891-a50f-1faf41c5992f" width="40%">
  <img src="https://github.com/user-attachments/assets/47f4d448-bc84-4cbc-8562-4753542f0776" width="40%">
  <img src="https://github.com/user-attachments/assets/5b395af1-184f-49cd-bbfc-8fe543a4b20b" width="40%">
  <img src="https://github.com/user-attachments/assets/55a06acf-33d7-4405-8224-224113c36a78" width="40%">
</p>

## Overview

The Geolocation Radar is a simple tool for highlighting specific colors in satellite images. Instead of seeing everything in full color, this tool turns the image black and white, except for one chosen color (like red, green, or blue). This makes it easier to spot important details, like roof colors, vegetation, or other features that might blend into the background.

## Key Features

- **Works Anywhere** – Use it with any application, from your browser to **Google Earth Pro**.
- **Cross-Platform** – Runs on **Windows**, **macOS**, and **Linux**.
- **Flexible Window Modes** – Keep a small always-on-top window or expand it for side-by-side comparison.
- **Customizable Filters** – Add your own filters for specific geolocation needs.
- **Stream Deck Integration** – Quickly switch filters with the **OBS Stream Deck plugin**.


## Download
**Windows** | [GR_Windows.zip](https://github.com/thewitnesshub/geo_radar/releases/download/v1.0.0/GR_Windows.zip) |


**macOS** | [GR_Mac.zip](https://github.com/thewitnesshub/geo_radar/releases/download/v1.0.0/GR_Mac.zip) |


## Setup

<details>
  <summary><b>Windows</b> Installation</summary>

1. Download and install OBS Studio from [obsproject.com](https://obsproject.com/).
2. Download `GR-Windows.zip` from above and unzip it.
3. Copy the files from the `LUTs` folder into OBS’s LUT folder:
   ```
   C:\Program Files\obs-studio\data\obs-plugins\obs-filters\LUTs
   ```
- If OBS is installed somewhere else (for example, on E:\), find the correct LUT folder, copy the files there, and you’ll need to manually apply the LUTs in step 7.
4. In OBS, go to **Scene Collection > Import** and select `Geolocation_Radar.json`.
5. In **Scene Collection**, select **Geolocation Radar**.
6. In the **Sources** panel, double-click **Original Source** (or right-click and choose **Properties**) and select the window you want to capture.
*Tip: Make sure the window is open, or it won’t appear in the list.*

7. If the LUTs aren’t automatically detected, manually apply them for each color scene (red, green, blue):
- Right-click the scene (e.g., **red**) and choose **Filters**.
- Click **Apply LUT**, then click **Browse**.
- Navigate to the `LUTs` folder inside the extracted Geolocation Radar folder and select the matching `.png` file (for example, `red-isolated.png` for the red scene).

#### Start the Stream

1. In OBS, go to the **Sources** panel.
2. Double-click **Original Source** (or right-click and select **Properties**).
3. Choose the window or application you want to capture from the dropdown.
   - *Tip:* Make sure the window is open before you start, or it won’t show up in the list.

-- Happy geolocating! 🌍
</details>


</details>
<details>
<summary><b>macOS</b> Installation</summary>

1. Download and install OBS Studio from [obsproject.com](https://obsproject.com/).
2. Download `GR-Mac.zip` from above and unzip it.
3. Move the unzipped folder to an easy-to-find spot, like your **Documents** folder.  
*(Important: If you move it later, you'll need to reapply the LUT filters in OBS.)*
4. In OBS, go to **Scene Collection > Import** and select `Geolocation_Radar.json`.
5. Go back to **Scene Collection** and select **Geolocation Radar**.
6. In the **Sources** panel below, double-click **Original Source** (or right-click and select **Properties**).
7. Under **Method**, choose **Window Capture** if it's not already selected and choose the desired application from the list (ensure it’s open).
8. For each color scene (red, green, blue):
   - Right-click the scene and choose **Filters**.
   - Click **Apply LUT**.
    - Browse to the `LUTs` subfolder inside the extracted Geolocation Radar folder and select the corresponding `.png` file (e.g., `red-isolated.png` for the red scene).

-- Happy geolocating! 🌍
</details>


</details>

## Usage

<details>
  <summary>Switch Between Color Filters 🔴🟢🔵 </summary>
   <br>
   
1. In OBS, find the **Scenes** panel on the bottom left.
2. Click on:
   - **Original** → See the image **without any filters**.
   - **Red / Green / Blue** → View the image with only the **selected color** visible.

</details>
<details>
  <summary>Open a Windowed Preview 🖥️</summary>
   <br>
   
1. **Right-click** on the stream preview.
2. Select **"Windowed Projector (Preview)"** to open a separate floating preview window.

💡 **Optimize Performance**  
- **Right-click** on the preview window again.  
- Turn off **"Enabled Preview"** (this prevents OBS from running two previews at once).

</details>
<details>
  <summary>Keep the Preview Window Always on Top 📌</summary>
   <br>
   
1. **Right-click** on the Windowed Preview.  
2. Click **"Always on Top"** to keep it visible while working in other apps.

</details>

## Troubleshooting

<details>
  <summary>Stream looks blurry</summary>
   <br>
  
By default, the resolution is set to **1920x1080**, which might look blurry on high-resolution screens. If your computer can handle a higher resolution, follow these steps to improve clarity:
<br>

1. Open OBS and click **Settings** (bottom-right corner).
2. Go to the **Video** tab (left panel).
3. Find **Base (Canvas)** Resolution and **Output (Scaled)** Resolution:
4. For 4K screens (3840x2160) → Set both to **3840x2160**.
5. For Full HD screens (1920x1080) → Set both to **1920x1080**.
7. Click **Apply**, then **OK**.

If the changes don’t apply immediately, restart OBS.

</details>
<details>
  <summary>Stream is zoomed in</summary>
  <br>
  If parts of your screen are missing or the stream appears zoomed in, try the following steps:

  1. **Adjust the Preview Scaling:**  
     Below the preview screen, where it shows something like **Canvas (1920 x 1080)**, click it and select **"Scale to Window"**.

  2. **Fit the Source to the Screen:**  
     If the image is still cropped, right-click the problematic source in OBS, then choose **Transform > Fit to Screen**  
     *(Shortcut: Ctrl+F on Windows or Cmd+F on Mac)*.

  3. **Reset the Transform (if needed):**  
     If the image still looks off, right-click the source again and select **Transform > Reset Transform**.

  4. **Repeat for Each Scene:**  
     These changes may need to be applied to each scene individually.
</details>
<details> 
  <summary>The filters are not working/colors are wrong</summary> 
  <br> 
  <p align="left">
  <img src="https://github.com/user-attachments/assets/2dadc9dc-cc80-4d15-ab22-0ce6947b749d" width="40%">
</p>
  If the filters aren’t applied correctly or the colors appear off, it typically means that the LUT files (the `.png` files) are missing or have been moved. To resolve this issue for each color scene (red, green, blue), follow these steps:
  
  1. **Right-click the scene** (e.g. red) and choose **Filters**. 

  2. Click **Apply LUT**. 

  3. **Browse** to the `LUTs` subfolder inside the extracted Geolocation Radar folder (or wherever you moved them) and select the corresponding `.png` file (for example, `red-isolated.png` for the red scene). 
     Repeat these steps for each color scene to ensure the correct LUT is applied. 
</details>


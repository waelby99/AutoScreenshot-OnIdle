# Screenshot Capture on Inactivity  

> **Note:** This project is a work in progress. I am currently working on extending the functionality so that the screenshot captures the entire monitor (all visible screens) instead of just the current browser tab.

## Overview  

This project is a simple web page that automatically takes a screenshot of the page if the user is inactive for 5 seconds. It uses the `html2canvas` library to create a snapshot of the current state of the page.

## Features  

- Detects user inactivity (no mouse movement or keyboard activity).  
- Automatically captures a screenshot of the page after 5 seconds of inactivity.  
- Allows users to download the captured screenshot as a PNG file with a single click.  

## Upcoming Feature  

- **Full Monitor Screenshot**: The ability to capture the entire monitor's content (including other tabs or windows). Stay tuned for updates!  

## Technologies Used  

- **HTML5**: For the structure of the web page.  
- **JavaScript**: For handling user inactivity and triggering the screenshot capture.  
- **html2canvas**: A library to convert the current page into a canvas element.  

## How It Works  

1. **Inactivity Detection**: The page listens for `mousemove` and `keydown` events. When these events occur, the inactivity timer resets.  
2. **Screenshot Capture**: If the user is inactive for 5 seconds, the `html2canvas` library generates a screenshot of the page's content.  
3. **Download Screenshot**: A temporary download link is created to save the screenshot as a PNG file.  

## How to Use  

1. Open the `index.html` file in a browser.  
2. The page will monitor user activity:  
   - Move your mouse or press any key to reset the inactivity timer.  
3. If no activity is detected for 5 seconds, a screenshot is automatically captured.  
4. Click the "Télécharger la capture" button to manually trigger the screenshot download.  

## Project Structure  

```plaintext  
project-directory/  
│  
├── index.html     # Main HTML file  
├── README.md      # Project documentation  
└── html2canvas.min.js # External library (loaded via CDN)  
```

## Installation 

1. Clone or download this repository.
2. Open index.html in a modern web browser.

##  Dependencies
- html2canvas: A JavaScript library used for creating screenshots.

The html2canvas library is loaded via a CDN:
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>  
```

## Customization
 - Adjust Inactivity Timeout: Modify the 5000 value in the script to change the inactivity duration (in milliseconds).
 - Change Download Filename: Update the link.download property to set a different name for the downloaded file.

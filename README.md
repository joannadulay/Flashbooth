# Flashbooth

Flashbooth is a browser-based photobooth application that allows users to take photos using their device camera, apply visual effects, create photo strips, customize captured images, and save their results in a gallery.

The project is designed as a lightweight, client-side photobooth experience that runs directly in a modern web browser without requiring a backend server.

## Features

### Camera and Photo Capture

- Uses the device camera through the browser's camera API.
- Displays a live camera preview.
- Supports taking individual photos.
- Supports a photo strip mode with selectable photo counts:
  - 2 photos
  - 3 photos
  - 4 photos
  - 6 photos
- Includes a countdown before taking photos.
- Supports mirrored camera preview.
- Includes shutter sound controls.

### Photo Filters and Adjustments

- Apply visual filters to the camera preview and captured photos.
- Adjust the image crop and size.
- Use different framing options.
- Preview the result before saving it.

### Photo Strip Customization

- Create photo strips using multiple captured images.
- Choose from several strip designs and color themes.
- Customize the strip after taking the photos.
- Add doodles or drawings to the strip.
- Select a doodle color.
- Adjust brush size.
- Undo drawing actions.
- Clear all doodles.
- Save the customized strip.
- Save the strip without doodles.

### Gallery and Lightbox

- View captured photos and photo strips in a gallery.
- Open images in a larger lightbox view.
- Download captured photos.
- Download generated photo strips.
- Delete unwanted gallery entries.

## Technologies Used

- **HTML5** — application structure and interface.
- **CSS3** — layout, styling, themes, animations, and responsive design.
- **JavaScript** — camera handling, photo capture, filters, countdowns, gallery behavior, strip generation, and doodle editing.
- **MediaDevices API** — access to the user's camera through `navigator.mediaDevices.getUserMedia()`.
- **Canvas API** — image composition, photo strip generation, drawing, and image processing.
- **Browser File APIs** — handling captured image data and downloads.
- **Google Fonts** — Fraunces and Space Grotesk for the visual design.

## Requirements

To run Flashbooth, you need:

- A modern browser such as Google Chrome, Microsoft Edge, Firefox, or Safari.
- A device with a camera for live photo capture.
- Camera permission enabled for the website.
- A secure browser context, usually:
  - `https://`, or
  - `localhost` during local development.

Camera access may not work when the file is opened directly using a `file://` URL, depending on the browser.

## Running the Project

### Option 1: Open with a Local Development Server

Place `flashbooth_updated.html` in a project folder, then start a local server.

For Python:

```bash
python -m http.server 8000
```

Open the following address in your browser:

```text
http://localhost:8000/flashbooth_updated.html
```

### Option 2: Use a Code Editor Extension

If using Visual Studio Code:

1. Open the project folder.
2. Install the **Live Server** extension.
3. Right-click `flashbooth_updated.html`.
4. Select **Open with Live Server**.
5. Allow camera access when prompted.

## How to Use

### Taking a Single Photo

1. Open Flashbooth in a supported browser.
2. Allow camera access.
3. Position yourself in the camera preview.
4. Select the desired filter or frame.
5. Adjust the crop or image size if needed.
6. Press the photo capture button.
7. Wait for the countdown to finish.
8. Review the captured image.
9. Save the image to the gallery or download it.

### Creating a Photo Strip

1. Switch to photo strip mode.
2. Select the number of photos.
3. Select a strip design or color theme.
4. Start the photo strip session.
5. Follow the countdown for each photo.
6. Review the completed strip.
7. Open the strip editor if you want to add doodles.
8. Draw on the strip using the selected brush color and size.
9. Use **Undo** or **Clear Doodles** if necessary.
10. Save the customized strip or save it without doodles.

### Managing the Gallery

- Select a gallery item to view it.
- Use the lightbox for a larger preview.
- Download images you want to keep.
- Delete images that are no longer needed.

## Project Structure

The current working version is contained in a single HTML file:

```text
Flashbooth/
└── flashbooth_updated.html
```

The file contains:

- Page markup and interface controls.
- Embedded CSS styles.
- Camera preview logic.
- Photo capture logic.
- Filter and frame handling.
- Photo strip generation.
- Strip customization tools.
- Canvas drawing tools.
- Gallery and lightbox behavior.
- Download and delete actions.

## Main Interface Components

The application includes controls and interface sections for:

- Camera preview
- Capture button
- Countdown display
- Camera mode selection
- Filter selection
- Frame selection
- Crop and size controls
- Mirror toggle
- Sound toggle
- Photo strip settings
- Strip count selection
- Strip design selection
- Strip editor
- Doodle color picker
- Brush size control
- Undo and clear controls
- Gallery
- Image lightbox

## Design

Flashbooth uses a dark burgundy and cream visual style, supported by:

- Rounded interface elements
- Soft contrast between panels and controls
- Editorial-style typography
- Fraunces for display text
- Space Grotesk for interface text
- Responsive layouts for desktop and smaller screens

## Browser Permissions

Flashbooth requires camera permission to display the live camera preview and capture photos.

If the camera does not appear:

1. Check that the browser has camera permission.
2. Confirm that another application is not using the camera.
3. Use `localhost` or an HTTPS connection.
4. Reload the page after granting permission.
5. Check the browser's site permissions.

## Limitations

- The application currently runs entirely in the browser.
- Captured content is handled on the client side.
- Camera behavior depends on browser support and device permissions.
- Image quality depends on the device camera and browser capabilities.
- Some camera features may behave differently on mobile and desktop browsers.
- The working version includes photo strips and doodle editing, but advanced Live Photo-style motion playback is not part of this stable version.
- The application does not currently include a backend database or user account system.

## Future Improvements

Possible future enhancements include:

- Reliable iPhone-style Live Photo capture and playback.
- A visible Live Photo badge on compatible gallery items.
- Short motion previews before and after capture.
- More frame and strip templates.
- Text and sticker overlays.
- Additional image adjustment controls.
- Cloud storage and account synchronization.
- Export options for GIF and video formats.
- Improved mobile camera support.
- Sharing directly to social media.
- Persistent gallery storage using IndexedDB.

## Project Status

**Current status:** Working browser-based photobooth prototype.

The stable version focuses on camera capture, photo filters, photo strips, strip customization, doodles, gallery viewing, and downloading.

## License

No license has been specified for this project yet. Add an appropriate license if the project will be distributed publicly.

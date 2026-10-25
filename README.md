# CallSpace

CallSpace is a browser-based contact manager with a simulated calling interface. It lets you save contacts, attach profile and call-screen images, and switch between saved images during a call-style experience.

## Features

- **Contact management:** Add, edit, and search contacts by name or phone number.
- **Profile pictures:** Add an optional profile picture for each contact.
- **Call-screen images:** Save four optional images for each contact: Original, Left, Right, and Back.
- **Simulated calls:** Select **Call** to open a call screen. The interface displays a calling animation for about three seconds before showing the connected-style screen. This is a visual simulation; it does not place real phone calls.
- **Swipe navigation:** Swipe horizontally across the call image area to switch between the saved image positions. A vertical swipe returns to the Original image.
- **Local saving:** Contacts are saved in browser storage on the device, using Local Storage and IndexedDB where available.
- **Import and export:** Export contacts to a `callspace-contacts.json` file, or import contacts from a compatible JSON file.
- **Fullscreen mode:** Expand the app to fullscreen when the browser supports it.
- **Image processing:** Selected photos are resized and converted to JPEG for more compact storage. HEIC/HEIF images may be converted with the help of the externally loaded `heic2any` library.

## How to Use

1. Open the HTML file in a compatible browser.
2. Add a contact with a name. A phone number and images are optional.
3. Choose **Save contact**. To change an existing contact, use its menu button and update the details.
4. Use the search field to filter the contact list.
5. Select **Call** to open that contact's simulated call screen.
6. While the call screen is connected, swipe across the image area to view the Left, Right, and Back images.
7. Use **End call** to return to the contact list.
8. Use **Export** to back up contacts or **Import** to add contacts from a JSON backup.

## Data and Compatibility Notes

- Contact data is intended to remain on the current device and browser. Clearing browser data, using another browser, or opening the file in a different environment may make saved contacts unavailable. Export backups regularly if the contacts matter.
- Importing adds contacts from the selected JSON file; it does not replace the existing contact list.
- The app relies on browser support for Local Storage, IndexedDB, file inputs, image processing, and fullscreen APIs. Some embedded browsers may restrict these features.
- HEIC/HEIF conversion loads a JavaScript library from a CDN, so an internet connection may be required for that conversion feature. Standard JPG and PNG images are preferable if the library cannot load.
- The app provides a call-style visual experience only. It does not connect to phone networks or make actual calls.


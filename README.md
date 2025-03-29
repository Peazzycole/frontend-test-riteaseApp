## Overview

The Document Signer & Annotation Tool is a modern web application built with Next.js that allows users to upload, annotate, and export PDF documents seamlessly. Designed with a sleek and intuitive interface, this tool empowers users to highlight, underline, comment, and sign documents with ease. Whether you're reviewing contracts, collaborating on reports, or signing important files, this application provides all the tools you need in one place.

### Key Features:
- **PDF Upload**: Drag-and-drop or select files to upload and view PDFs instantly.
- **Annotation Tools**: Highlight, underline, comment, and draw signatures directly on the document.
- **Export Functionality**: Save annotated PDFs with all changes embedded while maintaining high quality.
- **Responsive Design**: Optimized for use across devices, from desktops to mobile screens.
- **Smooth User Experience**: Fast, single-page application with real-time updates and feedback.

Built with cutting-edge technologies like React, Tailwind CSS, and pdf-lib, this project demonstrates the power of modern web development to create efficient and user-friendly tools.

### Setup Instructions

1. **Clone the repository**  
   ```bash
   https://github.com/Peazzycole/frontend-test-riteaseApp.git
   ```
2.  - cd your-repo
3. ```bash
      #run
      npm install
      #or run
      yarn install
   ```
4. After installation run
   ```bash
      npm run dev
      #or
      yarn dev
   ```
   The app should now be running at http://localhost:3000

### Tools Used
1. **Framer Motion:** I Used this for animations and transitions, such as sidebar animations and notification popups.

2. **lucide-react**: This Provides SVG-based icons used in the UI, such as file upload and alert icons.

3. **pdf-lib**: I Used this library for manipulating the PDF file, such as embedding annotations and exporting the annotated PDF.

4. **react-dropzone**: I Used this for implementing drag-and-drop functionality and also for uploading PDF files.

5. **react-icons**: This library Provides a collection of icons used in the UI, such as annotation and tool icons.

6. **react-pdf**: This I Used for rendering PDF documents in the browser.

7. **uuid**: Used this to generate unique IDs for annotations.

### Challenges Faced and How They Were Solved

1. **PDF Rendering Issues**: 
   - **Challenge**: Had issues rendering the PDF initially with react-pdf.
   - **Solution**: Checked the react-pdf docs and other implementations online to see how others did it, and fixed my code using with those refrences.

2. **Annotation Positioning**: 
   - **Challenge**: Ensuring annotations were accurately placed on the PDF, especially when resizing the viewport.
   - **Solution**: Normalized annotation coordinates relative to the PDF viewport and recalculated positions dynamically.

3. **Exporting Annotated PDFs**: 
   - **Challenge**: Embedding annotations and signatures into the exported PDF while maintaining the quality of the original document and also making sure the comment show up in the PDF.
   - **Solution**: Used `pdf-lib` to programmatically embed annotations, comments and signatures into the PDF, ensuring they were properly aligned and preserved. The comment was the real challenge as they will show up in the                   downloaded PDF but the content won't. Found out the fix was just to wrap the Content with PDFString.of(comment).

4. **Responsive Design**: 
   - **Challenge**: Making the application fully responsive across different screen sizes and devices.
   - **Solution**: Utilized Tailwind CSS to create a responsive layout and tested the application on various devices to ensure compatibility. And also implemented different sidebars based on the screensize

5. **Drag-and-Drop Functionality**: 
   - **Challenge**: Implementing a seamless drag-and-drop feature for uploading PDF files.
   - **Solution**: Used `react-dropzone` to handle drag-and-drop events and uploading PDFs, this made life easy as it was straightforward to set up.

### Features to Add If More Time Was Available

1. **Zoom Functionality**: Allow users to zoom in and out of the PDF for better readability and precision when annotating.
2. **Full-Page Mode**: Add a feature to view the PDF in full-page mode for an immersive reading experience.
3. **Light and Dark Mode**: Provide a toggle for light and dark modes to cater to different user preferences and improve accessibility.
4. **Page Navigation**: Enable users to navigate directly to a specific page by entering the page number, making it easier to work with large documents.
5. **Annotation History**: Add an undo/redo feature to let users easily revert or reapply changes to their annotations.
6. **Customizable Annotation Tools**: Allow users to customize annotation tools, such as setting default colors, line thickness, or font sizes.
7. **Save Progress**: Implement a feature to save annotation progress locally or in the cloud, so users can resume their work later.
8. **Search Functionality**: Add the ability to search for specific text within the PDF for quick navigation.
9. **Mobile Optimization**: Enhance the mobile experience with touch-friendly controls for annotations and navigation.


# Task Squirrel - Lab 1

Task Squirrel is an app that helps parents manage and assign tasks to their children, requiring them to attach photos as proof of task completion. This project implements several features related to photo selection and displaying the location of the photo on a map.

## Features Implemented

### 1. Task List View
- **View a list of tasks**: The app displays a list of tasks that need to be completed. Each task shows the title and an image indicating its completion status.
- **Task Data Model**: The `Task` model includes properties for `title`, `description`, `image` (of type `UIImage?`), and `isComplete` (a computed property that returns true if `image` is non-nil).

### 2. Task Detail View
- **Task Details**: Tapping on a task from the list navigates to the detail view, showing the task's title, description, and a completion indicator.
- **Attach Photo**: If no photo is attached to a task, an "Attach Photo" button is displayed. This button allows users to select a photo from their photo library.

### 3. Photo Selection and Metadata Access
- **PHPickerViewController Integration**: Implemented a photo picker using `PHPickerViewController` to allow users to select a photo from their library.
- **Photo Library Authorization**: Added functionality to request and handle user authorization for accessing the photo library.
- **Metadata Extraction**: Extracted the location metadata from the selected photo using the `PHAsset` API.

### 4. Map View
- **Display Photo Location**: After attaching a photo to a task, the app displays a map showing the location where the photo was taken.
- **Map Zoom**: The map zooms in on the specific location associated with the photo's metadata.
- **Custom Annotation**: Added a custom annotation to the map that displays the selected image as a pin.

### 5. Custom Annotation View
- **TaskAnnotationView**: Implemented a custom `MKAnnotationView` subclass to replace the default map pin with a custom view showing the attached photo.

## Setup Instructions

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/TaskSquirrel.git
    ```
2. Open the project in Xcode.
3. Run the app on a physical iOS device or simulator.
4. Add tasks, attach photos, and view the location of each photo on the map.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

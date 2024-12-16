# Cursor Desktop Image for Ubuntu

Create a desktop image for Cursor on Ubuntu.

## Installation

### 1. Install Cursor

- **Download Cursor AppImage** from [https://www.cursor.com/](https://www.cursor.com/).
  
- **Rename the AppImage:**
    ```bash
  mv <path_to_downloaded_cursor_appimage> cursor.AppImage 
  ```

- **Make it executable and move to `/opt`:**
    ```bash
  chmod +x cursor.AppImage
  sudo mv cursor.AppImage /opt/cursor.AppImage
   ```

### 2. Install FUSE
- Install FUSE support required by the AppImage:

	```bash
	sudo apt-get install libfuse2
	```

### 3. Add Desktop Entry

- **Clone the Repository:**

  ```bash
  git clone git@github.com:RobinSchmid7/cursor_desktop.git
  cd cursor_desktop
  ```

- **Copy Files:**

  ```bash
  sudo cp cursor.desktop /usr/share/applications/cursor.desktop
  sudo cp cursor.png /opt/cursor.png
  ```

## Running Cursor

Launch Cursor using the following command:

```bash
/opt/cursor.AppImage
```

Alternatively, you can find Cursor in your application menu after adding the desktop entry.


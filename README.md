# Markdown Notes Extension

A Visual Studio Code extension that allows you to create, edit, and manage Markdown notes directly from the sidebar.

## Features

- **Sidebar Integration**: Access your notes from the Explorer sidebar
- **Create Notes**: Easily create new Markdown notes with custom titles
- **Edit Notes**: Click on any note to open it in a Markdown editor
- **Auto-Save**: Notes are automatically saved as you type
- **Delete Notes**: Remove notes you no longer need
- **Persistent Storage**: Notes are saved globally and persist across VS Code sessions
- **Preview**: See a preview of your note content in the sidebar

## How to Use

1. **View Notes**: Look for the "Markdown Notes" panel in the Explorer sidebar
2. **Create a Note**: Click the "+" icon in the panel header or use the "Create your first note" link
3. **Edit a Note**: Click on any note in the list to open it in the editor
4. **Delete a Note**: Right-click on a note and select "Delete Note" or click the trash icon
5. **Refresh**: Click the refresh icon to reload your notes

## Installation

### Install from Package (Recommended)

The extension is available as a pre-built package file: `markdown-notes-0.0.1.vsix`

#### Option 1: Command Line Installation
```bash
code --install-extension markdown-notes-0.0.1.vsix
```

#### Option 2: VS Code GUI Installation
1. Open Visual Studio Code
2. Go to Extensions (Ctrl+Shift+X or Cmd+Shift+X)
3. Click the "..." menu (More Actions) in the top-right
4. Select "Install from VSIX..."
5. Browse and select the `markdown-notes-0.0.1.vsix` file
6. Click "Install" and reload VS Code when prompted

#### Option 3: Command Palette Installation
1. Open Command Palette (Ctrl+Shift+P or Cmd+Shift+P)
2. Type "Extensions: Install from VSIX..."
3. Select the command and browse to the `.vsix` file
4. Select the file and confirm installation

### From Source (Development)

1. Clone or download this extension source code
2. Open the folder in VS Code
3. Run `npm install` to install dependencies
4. Press `F5` to run the extension in a new Extension Development Host window
5. Look for "Markdown Notes" in the Explorer sidebar

### Building Your Own Package

1. Install `vsce` globally: `npm install -g @vscode/vsce`
2. Run `vsce package` to create a `.vsix` file
3. Install the generated extension using any of the methods above

### After Installation

Once the extension is installed:
1. Restart VS Code (if required)
2. Look for "Markdown Notes" in the Explorer sidebar
3. If you don't see it, try:
   - Opening the Explorer panel (Ctrl+Shift+E)
   - Scrolling down in the Explorer sidebar
   - Right-clicking in the Explorer and checking if "Markdown Notes" is available

## Development

### Project Structure

- `src/extension.ts` - Main extension entry point
- `src/markdownNotesProvider.ts` - Tree data provider for the sidebar
- `src/markdownNote.ts` - Note data model
- `src/notesStorage.ts` - Storage handling for persistence
- `package.json` - Extension manifest and configuration

### Commands

- `markdownNotes.createNote` - Create a new note
- `markdownNotes.deleteNote` - Delete an existing note
- `markdownNotes.refreshNotes` - Refresh the notes list
- `markdownNotes.openNote` - Open a note for editing

## Requirements

- Visual Studio Code 1.74.0 or higher

## Troubleshooting

### Extension Not Appearing
If the "Markdown Notes" panel doesn't appear in the Explorer sidebar:
1. Make sure the extension is installed and enabled in the Extensions view
2. Try reloading VS Code (Ctrl+Shift+P → "Developer: Reload Window")
3. Check if the Explorer panel is open (Ctrl+Shift+E)
4. Look for "Markdown Notes" at the bottom of the Explorer sidebar

### Installation Issues
If you encounter issues during installation:
1. Make sure you have the latest version of VS Code
2. Try installing via a different method (GUI vs Command Line)
3. Check the Output panel for error messages (View → Output)

### Notes Not Saving
If notes aren't being saved:
1. Check VS Code's permissions to write to its configuration directory
2. Try creating a new note to test the functionality
3. Restart VS Code and check if notes persist

## License

This project is open source. Feel free to contribute improvements and bug fixes!

# Data Workflow Visualization

This project is a web-based visualization tool for representing a data workflow using a tree structure. It also includes an interactive chatbot feature to provide information about the nodes in the workflow.

## Features

1. **Data Workflow Visualization**:
   - Displays a tree structure representing various stages of a data workflow.
   - Nodes represent different stages like "Data Processing," "Data Cleaning," etc.
   - Links connect the nodes to show relationships between stages.

2. **Interactive Elements**:
   - Nodes are interactive and display details when clicked.
   - Hovering over nodes highlights them and shows a tooltip with the node's name.

3. **Chatbot**:
   - A chatbot named "Alex Chatbot" answers questions about the workflow nodes.
   - Users can type questions, and the chatbot provides descriptions of the nodes.
   - Chat history is displayed and can be edited or deleted.
   - Chat history can be saved as a text file.

4. **Zoom and Pan**:
   - The visualization supports zooming and panning for better navigation.

## Code Overview

### HTML Structure
- The main elements include:
  - An `<svg>` element for rendering the tree visualization.
  - A tooltip `<div>` for displaying node information on hover.
  - A note box `<div>` for showing details of the selected node.
  - A chatbot `<div>` for user interaction.

### CSS Styling
- The page uses a dark theme with green and blue accents.
- Nodes, links, tooltips, and chatbot elements are styled for a clean and modern look.

### JavaScript Functionality
#### Visualization
- **Tree Layout**:
  - The tree structure is created using D3.js.
  - The `d3.tree()` layout is used to position nodes and links.
- **Zoom and Pan**:
  - Implemented using `d3.zoom()` to allow users to navigate the visualization.

#### Node Interaction
- Clicking a node updates the note box with the node's name.
- Hovering over a node changes its color and displays a tooltip.

#### Chatbot
- The chatbot listens for user input and matches queries with node names.
- Responses include descriptions of the nodes.
- Chat history is managed in an array and rendered dynamically.
- Users can edit or delete chat messages.
- A "Save Chat History" button allows users to download the chat history as a text file.

### Key Functions
1. **`renderChatHistory()`**:
   - Updates the chatbot's response area with the current chat history.
2. **`editMessage(index)`**:
   - Allows users to edit a specific chat message.
3. **`deleteMessage(index)`**:
   - Deletes a specific chat message from the history.
4. **`saveChatHistory()`**:
   - Saves the chat history to a text file.

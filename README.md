## 🚀 Assignment Tasks Implementation

I have successfully implemented all three core tasks as per the internship requirements:

### 1. Advanced Sorting & Filtering
- **Functionality:** Added a dropdown menu (▼) in each column header.
- **Sorting:** Supports Ascending (A-Z) and Descending (Z-A) order.
- **Filtering:** Integrated a real-time search box within the header menu to filter rows based on specific column values.
- **Technical Detail:** Implemented sorting and filtering at the view-layer using `useMemo` to ensure that underlying formula references remain stable.

### 2. Multi-Cell Copy-Paste
- **Range Support:** Supports copying ranges from external tools like Excel/Google Sheets and pasting them directly into the grid.
- **Logic:** Implemented a tab-delimited parser in `handlePaste` that maps clipboard data into multiple engine cells starting from the selected anchor.

### 3. Data Persistence (Auto-Save)
- **Local Storage:** The entire spreadsheet state (cell values + formatting) is saved automatically to the browser's `localStorage`.
- **Restoration:** On page refresh, data is reconstructed into the engine using a custom-built restoration logic that ensures zero data loss.
- **Error Handling:** Built a fail-safe iteration method to bypass `Object.fromEntries` limitations, ensuring the app never crashes during the save cycle.

## 🎨 UI Enhancements
- **Excel-inspired Headers:** Dropdown buttons match the cell background for a clean, professional look.
- **Active States:** Bold, Italic, and Alignment buttons show active states based on the selected cell's properties. 
- **Responsive Grid:** Optimized for smooth scrolling with a large number of rows and columns.
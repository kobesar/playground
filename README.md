# Data Visualization Playground

A fully-featured, browser-based data visualization tool built with D3.js v7.

## 🚀 Quick Start

1. **Open the app**: Simply open `data-viz-playground.html` in any modern browser (Chrome, Firefox, Safari, Edge)
2. **No build tools required**: Everything runs directly in the browser
3. **Test with sample data**: Use the provided `sample-data.csv` or `sample-data.json` files

## ✨ Features

### Core Functionality
- **📁 File Upload**: Support for CSV and JSON datasets
- **👀 Data Preview**: Automatic table preview of uploaded data
- **📊 Multiple Chart Types**:
  - Bar Charts
  - Scatter Plots
  - Line Graphs
- **🎯 Interactive Controls**:
  - Column selection for X/Y axes
  - Optional grouping variables
  - Chart type switching

### Styling & Customization
- **🎨 Color Schemes**: 4 predefined color palettes (Default, Ocean, Sunset, Forest)
- **🖌️ Style Panel**:
  - Background color picker
  - Adjustable font size
  - Grid line toggles
  - Legend visibility
  - Custom chart titles

### Interactive Features
- **💬 Tooltips**: Hover over data points to see detailed values
- **✨ Smooth Transitions**: Animated chart rendering and updates
- **🎭 Visual Feedback**: Interactive hover effects

### Export/Import
- **💾 Export Configuration**: Save your visualization setup as JSON
- **📸 Export SVG**: Download charts as SVG files
- **📥 Import Configuration**: Reload saved configurations

## 📖 How to Use

### 1. Upload Data
Click the upload area or drag-and-drop a CSV or JSON file.

**CSV Format:**
```csv
name,value,category
Item A,30,Group1
Item B,80,Group2
Item C,45,Group1
```

**JSON Format:**
```json
[
  {"name": "Item A", "value": 30, "category": "Group1"},
  {"name": "Item B", "value": 80, "category": "Group2"},
  {"name": "Item C", "value": 45, "category": "Group1"}
]
```

### 2. Configure Visualization
- Choose chart type (bar, scatter, or line)
- Select columns for X and Y axes
- Optionally select a grouping column for color-coding

### 3. Customize Styling
- Pick a color scheme
- Adjust background color and font size
- Toggle grid lines and legend
- Add a custom title

### 4. Generate Chart
Click "Generate Visualization" to create your interactive chart

### 5. Export Your Work
- Save configuration to reuse later
- Export charts as SVG images

## 🎯 Example Use Cases

### Sales Analysis
- **X-Axis**: Quarter (Q1, Q2, Q3, Q4)
- **Y-Axis**: Sales
- **Group By**: Product
- **Chart Type**: Line Graph

### Product Performance
- **X-Axis**: Product
- **Y-Axis**: Profit
- **Group By**: Region
- **Chart Type**: Bar Chart

### Correlation Analysis
- **X-Axis**: Sales
- **Y-Axis**: Profit
- **Group By**: Product
- **Chart Type**: Scatter Plot

## 🔧 Technical Details

- **D3.js Version**: 7.x (loaded from CDN)
- **No Dependencies**: Single HTML file with embedded CSS and JavaScript
- **Responsive Design**: Adapts to different screen sizes
- **Modern JavaScript**: Uses ES6+ features
- **Browser Compatibility**: Works in all modern browsers

## 💡 Tips

1. **Numeric vs. Text**: The app automatically detects numeric columns for appropriate scaling
2. **Data Sorting**: Line graphs automatically sort data by X-axis values
3. **Color Groups**: Use the "Group By" option to color-code your data by categories
4. **Live Updates**: Most controls update the visualization in real-time
5. **Smooth Transitions**: Charts animate when switching types or updating data

## 🎨 Color Schemes

- **Default**: Purple/Pink gradient (modern, professional)
- **Ocean**: Blue/Cyan gradient (cool, calming)
- **Sunset**: Red/Orange gradient (warm, energetic)
- **Forest**: Green gradient (natural, organic)

## 📝 Sample Data

The included `sample-data.csv` and `sample-data.json` files contain quarterly sales data for different products across regions. Try these combinations:

1. **Quarterly Sales Trend**: X=quarter, Y=sales, Group=product, Type=Line
2. **Product Comparison**: X=product, Y=profit, Group=region, Type=Bar
3. **Sales vs. Profit**: X=sales, Y=profit, Group=product, Type=Scatter

## 🚀 Advanced Features

### Configuration Export/Import
Save your visualization setup (axis selections, chart type, styling) as a JSON file and reload it later to quickly recreate visualizations.

### Live Styling
Change colors, fonts, and other visual properties while viewing your chart to see updates in real-time.

### Responsive Tooltips
Hover over any data point to see detailed information about that specific data item.

## 📄 License

This is a demonstration project - feel free to use and modify as needed!

---

Built with ❤️ using D3.js v7
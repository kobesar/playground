# AI-Powered Data Visualization Playground

A browser-based data visualization tool powered by lightweight LLMs and D3.js v7. Simply describe what you want to visualize in plain English, and let AI configure your charts automatically!

## 🚀 Quick Start

1. **Open the app**: Open `data-viz-playground.html` in any modern browser
2. **Choose your LLM**:
   - **Ollama (Recommended)**: Free, runs locally, no API key needed
   - **OpenAI GPT-3.5/4o-mini**: Cloud-based, requires API key
   - **Anthropic Claude Haiku**: Cloud-based, requires API key
3. **Upload data**: Use `sample-data.csv` or `sample-data.json`
4. **Describe your visualization**: "Show me sales trends over quarters grouped by product"
5. **Let AI do the rest**: The LLM automatically configures chart type, axes, colors, and titles!

## ✨ Key Features

### AI-Powered Generation
- **Natural Language Interface**: Describe visualizations in plain English
- **Multiple LLM Support**:
  - Ollama (local, free, privacy-focused)
  - OpenAI GPT-3.5 Turbo / GPT-4o Mini
  - Anthropic Claude 3.5 Haiku / Claude 3 Haiku
- **Smart Configuration**: AI analyzes your data and chooses optimal settings
- **Example Prompts**: Click-to-use examples for quick starts

### Core Functionality
- **File Upload**: CSV and JSON support with drag-and-drop
- **Data Preview**: Interactive table showing your dataset
- **3 Chart Types**: Bar charts, scatter plots, and line graphs
- **Dynamic Controls**: AI or manual column selection
- **D3.js v7**: Powered by the latest D3.js library

### Styling & Customization
- **4 Color Schemes**: Default, Ocean, Sunset, Forest
- **Live Style Panel**:
  - Background color picker
  - Font size adjustment (8-24px)
  - Grid line toggles
  - Legend visibility
  - Custom chart titles
- **Real-time Updates**: See changes instantly

### Interactive Features
- **Tooltips**: Hover for detailed data values
- **Smooth Animations**:
  - Bars grow from bottom up
  - Lines draw progressively
  - Points fade in smoothly
- **Responsive Design**: Adapts to screen size

### Export/Import
- **Export Configuration**: Save visualization settings as JSON
- **Import Configuration**: Reload saved configs
- **Export SVG**: Download charts as high-quality vector images

## 🤖 Setting Up LLMs

### Option 1: Ollama (Recommended for Privacy & Cost)

**Install Ollama:**
```bash
# Visit https://ollama.ai to download installer
# Or use package managers:

# macOS
brew install ollama

# Linux
curl -fsSL https://ollama.ai/install.sh | sh
```

**Pull a lightweight model:**
```bash
# Recommended: Llama 3.2 (1B or 3B)
ollama pull llama3.2

# Alternatives:
ollama pull phi3          # Microsoft Phi-3 (3.8B)
ollama pull gemma2:2b     # Google Gemma 2 (2B)
ollama pull qwen2.5:3b    # Alibaba Qwen 2.5 (3B)
```

**Run Ollama:**
```bash
ollama serve
```

The app will automatically connect to `http://localhost:11434`.

### Option 2: OpenAI

1. Get an API key from [platform.openai.com](https://platform.openai.com/api-keys)
2. Select "OpenAI GPT-3.5" in the LLM Provider dropdown
3. Enter your API key (starts with `sk-`)
4. Choose model: GPT-3.5 Turbo (cheaper) or GPT-4o Mini (better quality)

### Option 3: Anthropic Claude

1. Get an API key from [console.anthropic.com](https://console.anthropic.com/)
2. Select "Anthropic Claude Haiku" in the LLM Provider dropdown
3. Enter your API key (starts with `sk-ant-`)
4. Choose model: Claude 3.5 Haiku (recommended) or Claude 3 Haiku

## 📖 How to Use

### AI-Powered Workflow (Recommended)

1. **Upload your data** (CSV or JSON)
2. **Describe what you want**:
   - "Show sales by product as a bar chart"
   - "Compare profit across regions with different colors"
   - "Line graph showing sales trend over time"
   - "Scatter plot of sales vs profit"
3. **Click "Generate with AI"**
4. **Watch the magic happen!**

The AI will:
- Analyze your data columns
- Choose the best chart type
- Select appropriate axes
- Pick a color scheme
- Generate a descriptive title
- Render the visualization

### Manual Workflow (Advanced)

1. Upload data
2. Expand "Manual Controls (Advanced)"
3. Select chart type, X/Y axes, and grouping
4. Click "Generate Visualization"
5. Customize styling as needed

## 🎯 Example Prompts

Try these with the sample data:

### Trend Analysis
```
Show me how sales have changed over quarters
Line graph of profit trends by product
Display quarterly revenue growth
```

### Comparisons
```
Compare sales across different products as a bar chart
Show profit by region with different colors
Which product category performs best?
```

### Correlation
```
Plot sales against profit to find relationships
Scatter plot showing the correlation between sales and profit
Are sales and profit correlated?
```

### Custom Styling
```
Bar chart of quarterly sales with sunset color scheme
Show regional performance with ocean colors
Create a forest-themed visualization of product sales
```

## 📊 Data Format

### CSV Example
```csv
product,sales,region,quarter,profit
Laptop,12500,North,Q1,3200
Tablet,8900,South,Q1,2100
Phone,15600,East,Q1,4200
```

### JSON Example
```json
[
  {"product": "Laptop", "sales": 12500, "region": "North", "quarter": "Q1", "profit": 3200},
  {"product": "Tablet", "sales": 8900, "region": "South", "quarter": "Q1", "profit": 2100},
  {"product": "Phone", "sales": 15600, "region": "East", "quarter": "Q1", "profit": 4200}
]
```

## 🔧 Technical Details

- **D3.js Version**: 7.x (loaded from CDN)
- **LLM Integration**: Direct API calls via fetch
- **No Build Tools**: Single HTML file, runs anywhere
- **No Backend**: Everything runs in the browser
- **Privacy**: Ollama keeps all data local
- **Browser Support**: Chrome, Firefox, Safari, Edge (modern versions)

## 💡 Tips & Tricks

### For Best AI Results
1. **Be specific**: "Bar chart of sales by product" works better than "show sales"
2. **Mention grouping**: "Compare X across Y" tells AI to use grouping
3. **Specify chart type**: Include "bar chart", "line graph", or "scatter plot"
4. **Request colors**: Ask for specific color schemes (ocean, sunset, forest)

### Performance
- Ollama models (1-3B parameters) respond in 1-3 seconds on modern hardware
- Cloud APIs (OpenAI, Anthropic) respond in <1 second
- D3.js renders charts smoothly with datasets up to 10,000 rows

### Privacy Considerations
- **Ollama**: All data stays on your machine
- **Cloud APIs**: Data sent to OpenAI/Anthropic servers
- **API Keys**: Stored only in browser session (not persisted)

## 🎨 Customization

### Color Schemes

Choose from 4 predefined palettes:
- **Default**: Modern purple/pink gradient
- **Ocean**: Cool blue/cyan tones
- **Sunset**: Warm red/orange hues
- **Forest**: Natural green shades

Or customize manually:
- Background color picker
- Font size slider
- Grid and legend toggles

### Manual Override

The AI picks good defaults, but you can always:
1. Expand "Manual Controls"
2. Adjust any setting
3. Re-render to see changes
4. Export your custom configuration

## 🚀 Advanced Usage

### Saving Workflows

1. Create a visualization you like
2. Click "Export Configuration"
3. Save the JSON file
4. Later: "Import Configuration" to restore

### Batch Processing

1. Upload dataset A, generate chart, export SVG
2. Upload dataset B, import config, export SVG
3. Consistent visualizations across multiple datasets!

### Custom LLM Endpoints

Using Ollama with custom settings:
```javascript
// Edit ollamaUrl in the app if running on different port
// Default: http://localhost:11434
```

## 🐛 Troubleshooting

### "Ollama error" when generating
- Ensure Ollama is running: `ollama serve`
- Check the model is installed: `ollama list`
- Pull the model if missing: `ollama pull llama3.2`

### "Please enter API key" for OpenAI/Anthropic
- Make sure you've entered your API key in the config panel
- Keys should start with `sk-` (OpenAI) or `sk-ant-` (Anthropic)

### Visualization not rendering
- Check data has numeric columns for Y-axis
- Try manual controls to verify data is loaded
- Open browser console (F12) for error messages

### Slow AI responses
- Ollama: Use smaller models (llama3.2:1b, gemma2:2b)
- Cloud APIs: Usually <1s, check network connection
- Large datasets: AI only sees sample row, but full dataset affects rendering

## 📚 Resources

- **D3.js Documentation**: [d3js.org](https://d3js.org)
- **Ollama**: [ollama.ai](https://ollama.ai)
- **OpenAI API**: [platform.openai.com](https://platform.openai.com)
- **Anthropic API**: [console.anthropic.com](https://console.anthropic.com)

## 🆚 LLM Comparison

| Provider | Cost | Speed | Privacy | Quality | Setup |
|----------|------|-------|---------|---------|-------|
| **Ollama** | Free | 1-3s | ✅ Local | Good | Install + Pull |
| **OpenAI GPT-3.5** | $0.002/1K | <1s | ☁️ Cloud | Excellent | API Key |
| **OpenAI GPT-4o Mini** | $0.006/1K | <1s | ☁️ Cloud | Excellent | API Key |
| **Claude Haiku** | $0.003/1K | <1s | ☁️ Cloud | Excellent | API Key |

**Recommendation**:
- **Privacy/Cost**: Use Ollama with llama3.2
- **Best Quality**: OpenAI GPT-4o Mini or Claude 3.5 Haiku
- **Balanced**: Ollama with phi3 or OpenAI GPT-3.5 Turbo

## 🎓 Example Workflow

```
1. Open data-viz-playground.html
2. Select "Ollama (Local, Free)"
3. Upload sample-data.csv
4. Type: "Show quarterly sales trends by product with ocean colors"
5. Click "Generate with AI"
6. Wait 2-3 seconds
7. View beautiful line graph with:
   - X-axis: quarter
   - Y-axis: sales
   - Grouped by: product
   - Color scheme: ocean
   - Title: "Quarterly Sales Trends by Product"
8. Tweak styling if needed
9. Export as SVG or save configuration
```

## 📄 License

This is a demonstration project - feel free to use and modify as needed!

---

**Built with ❤️ using D3.js v7 + AI**

*No servers, no build tools, just one HTML file and the power of LLMs!*
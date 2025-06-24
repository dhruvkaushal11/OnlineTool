# Professional Utility Tool Theme - Cursor Rules

## 🎨 Design System Overview
This theme provides a modern, professional design for online utility tools with gradient backgrounds, clean panels, and excellent UX.

## 🎯 When to Use
Apply these rules when building online utility tools like:
- JSON Formatter, XML Formatter, HTML Beautifier
- Code Converters, Validators, Minifiers  
- Text Processors, Encoders/Decoders
- API Testing Tools, Data Generators

## 🎨 Color Palette

### Primary Colors
```css
--primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
--header-gradient: linear-gradient(135deg, #2dd4bf 0%, #06b6d4 100%);
--white: #ffffff;
--light-bg: #f8fafc;
```

### Button Colors
```css
--btn-primary: #10b981;      /* Green - Primary actions */
--btn-primary-hover: #059669;
--btn-secondary: #6366f1;    /* Purple - Secondary actions */
--btn-secondary-hover: #4f46e5;
--btn-warning: #f59e0b;      /* Orange - Warning actions */
--btn-warning-hover: #d97706;
--btn-info: #0ea5e9;         /* Blue - Info actions */
--btn-info-hover: #0284c7;
```

### Text Colors
```css
--text-primary: #374151;     /* Dark gray - Primary text */
--text-secondary: #6b7280;   /* Medium gray - Secondary text */
--text-heading: #1f2937;     /* Very dark - Headings */
--text-muted: #9ca3af;       /* Light gray - Placeholders */
```

### Panel Colors
```css
--panel-header: #374151;     /* Dark gray - Panel headers */
--panel-bg: #ffffff;         /* White - Panel backgrounds */
--line-numbers: #f3f4f6;     /* Light gray - Line numbers */
--border-color: #e2e8f0;     /* Light border */
```

## 🏗️ Layout Structure

### Container
```css
.container {
    max-width: 1400px;
    margin: 0 auto;
    background: white;
    border-radius: 15px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.1);
    overflow: hidden;
}
```

### Header Pattern
```css
.header {
    background: var(--header-gradient);
    color: white;
    padding: 20px 30px;
    text-align: center;
}

.header h1 {
    font-size: 2.5rem;
    margin-bottom: 10px;
    font-weight: 300;
}

.header p {
    opacity: 0.9;
    font-size: 1.1rem;
}
```

### Main Content Layout
```css
.main-content {
    display: flex;
    height: 70vh;
    min-height: 500px;
    gap: 15px;
}

.panel {
    flex: 1;
    display: flex;
    flex-direction: column;
    min-width: 0;
    min-height: 0;
}
```

## 🎛️ Component Patterns

### Panel Headers
```css
.panel-header {
    background: var(--panel-header);
    color: white;
    padding: 15px 20px;
    font-weight: 600;
    font-size: 14px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

### Buttons
```css
.btn {
    padding: 12px 24px;
    border: none;
    border-radius: 8px;
    font-size: 14px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.btn:hover {
    transform: translateY(-2px);
}
```

### Control Panel (Center)
```css
.vertical-controls {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 15px;
    padding: 20px 10px;
    background: var(--light-bg);
    border-radius: 10px;
    min-width: 160px;
    max-width: 160px;
    border: 1px solid var(--border-color);
}
```

### Editors/Text Areas
```css
.editor {
    flex: 1;
    border: none;
    padding: 15px;
    font-family: 'Courier New', monospace;
    font-size: 16px;
    line-height: 1.6;
    background: white;
    color: var(--text-primary);
    overflow-y: auto;
    overflow-x: hidden;
    white-space: pre-wrap;
    word-wrap: break-word;
    word-break: break-all;
}

.editor:focus {
    outline: 2px solid #06b6d4;
    outline-offset: -2px;
}
```

### Line Numbers
```css
.line-numbers {
    background: var(--line-numbers);
    color: var(--text-secondary);
    padding: 15px 10px;
    font-family: 'Courier New', monospace;
    font-size: 16px;
    line-height: 1.6;
    text-align: right;
    border-right: 1px solid var(--border-color);
    min-width: 50px;
    user-select: none;
}
```

## 📱 Responsive Design

### Mobile Breakpoint
```css
@media (max-width: 768px) {
    .main-content {
        flex-direction: column;
        height: 80vh;
        min-height: 600px;
    }
    
    .vertical-controls {
        flex-direction: row;
        min-width: 100%;
        max-width: 100%;
        flex-wrap: wrap;
        justify-content: center;
    }
}
```

## 🎨 Syntax Highlighting Colors

### JSON/Code Syntax
```css
.json-key { color: #000000; font-weight: 600; }      /* Keys: Black bold */
.json-string { color: #22c55e; }                     /* Strings: Green */
.json-number { color: #3b82f6; font-weight: 500; }   /* Numbers: Blue bold */
.json-boolean { color: #f59e0b; font-weight: 600; }  /* Booleans: Orange bold */
.json-null { color: #ef4444; font-weight: 600; font-style: italic; } /* Null: Red italic */
.json-punctuation { color: #6b7280; }               /* Punctuation: Gray */
.json-bracket { color: #8b5cf6; font-weight: 600; }  /* Brackets: Purple bold */
```

## ⚡ Interactive Features

### Success/Error Panels
```css
.success-panel {
    background: #f0fdf4;
    border: 1px solid #bbf7d0;
    color: #166534;
    padding: 15px;
    margin: 20px 30px;
    border-radius: 8px;
    font-family: 'Courier New', monospace;
}

.error-panel {
    background: #fef2f2;
    border: 1px solid #fecaca;
    color: #dc2626;
    padding: 15px;
    margin: 20px 30px;
    border-radius: 8px;
    font-family: 'Courier New', monospace;
}
```

### Toggle Switches
```css
.toggle-switch {
    position: relative;
    width: 40px;
    height: 20px;
    background: rgba(255, 255, 255, 0.3);
    border-radius: 20px;
    cursor: pointer;
    transition: all 0.3s ease;
}

.toggle-switch.active {
    background: #10b981;
}

.toggle-slider {
    position: absolute;
    top: 2px;
    left: 2px;
    width: 16px;
    height: 16px;
    background: white;
    border-radius: 50%;
    transition: all 0.3s ease;
    box-shadow: 0 2px 4px rgba(0,0,0,0.2);
}

.toggle-switch.active .toggle-slider {
    transform: translateX(20px);
}
```

## 🔧 JavaScript Patterns

### Standard Functions to Include
```javascript
// Auto-save functionality
function saveToLocalStorage() { /* ... */ }
function loadFromLocalStorage() { /* ... */ }
function toggleAutoSave() { /* ... */ }

// UI Updates
function updateLineNumbers(type) { /* ... */ }
function showSuccess(message) { /* ... */ }
function showError(message) { /* ... */ }

// Copy functionality
function copyOutput() { /* ... */ }

// Smart editing (Tab/Enter keys)
function handleTabKey(e, editor) { /* ... */ }
function handleEnterKey(e, editor) { /* ... */ }
```

## 📋 Standard HTML Structure

### Basic Template
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- SEO Meta Tags -->
    <title>[Tool Name] - Free Online [Tool Type]</title>
    <meta name="description" content="Free online [tool description]">
    <!-- ... other meta tags -->
</head>
<body>
    <div class="container">
        <header class="header">
            <h1>Free Online [Tool Name]</h1>
            <p>[Tool description]</p>
        </header>
        
        <div class="main-content">
            <div class="panel">
                <div class="panel-header">
                    <span>Input [Type]</span>
                    <!-- Auto-save toggle -->
                </div>
                <div class="editor-container">
                    <div class="line-numbers" id="inputLineNumbers">1</div>
                    <div class="editor" id="inputEditor" contenteditable="true"></div>
                </div>
            </div>
            
            <div class="vertical-controls">
                <!-- Control buttons -->
            </div>
            
            <div class="panel">
                <div class="panel-header">
                    <span>Output [Type]</span>
                    <!-- Copy button -->
                </div>
                <div class="editor-container">
                    <div class="line-numbers" id="outputLineNumbers">1</div>
                    <div class="editor" id="outputEditor" contenteditable="true"></div>
                </div>
            </div>
        </div>
        
        <!-- Features section -->
        <!-- Footer -->
    </div>
</body>
</html>
```

## 🎯 Usage Instructions

1. **Copy the CSS variables** to your project
2. **Use the component patterns** for consistent UI elements
3. **Apply the layout structure** for the main content area
4. **Include standard JavaScript functions** for common functionality
5. **Follow the responsive design patterns** for mobile compatibility
6. **Use the color scheme** for buttons, text, and interactive elements

## 🚀 Quick Start Checklist

- [ ] Apply gradient background to body
- [ ] Create container with rounded corners and shadow
- [ ] Add gradient header with tool name and description
- [ ] Implement dual-panel layout with center controls
- [ ] Style buttons with hover effects
- [ ] Add line numbers and syntax highlighting
- [ ] Include success/error message panels
- [ ] Implement auto-save with toggle
- [ ] Add copy-to-clipboard functionality
- [ ] Make responsive for mobile devices

This theme ensures consistency across all your utility tools while maintaining a professional, modern appearance that users will recognize and trust.

## 🌐 Domain Configuration

### Production Domain
**Primary Domain:** `https://proximity-tools.com/`

### SEO Meta Tags Template
When creating new utility tools, always use the following URL structure:
- **Canonical URL:** `https://proximity-tools.com/[tool-name].html`
- **Open Graph URL:** `https://proximity-tools.com/[tool-name].html`
- **Twitter URL:** `https://proximity-tools.com/[tool-name].html`
- **Schema.org URL:** `https://proximity-tools.com/[tool-name].html`
- **Preview Images:** `https://proximity-tools.com/[tool-name]-preview.png`

### Standard Meta Tags
```html
<!-- Open Graph / Facebook -->
<meta property="og:type" content="website">
<meta property="og:url" content="https://proximity-tools.com/[tool-name].html">
<meta property="og:title" content="[Tool Name] - Free Online [Tool Type]">
<meta property="og:description" content="[Tool description]">
<meta property="og:image" content="https://proximity-tools.com/[tool-name]-preview.png">
<meta property="og:site_name" content="[Tool Name] Tool">

<!-- Twitter -->
<meta property="twitter:card" content="summary_large_image">
<meta property="twitter:url" content="https://proximity-tools.com/[tool-name].html">
<meta property="twitter:title" content="[Tool Name] - Free Online [Tool Type]">
<meta property="twitter:description" content="[Tool description]">
<meta property="twitter:image" content="https://proximity-tools.com/[tool-name]-preview.png">

<!-- Canonical URL -->
<link rel="canonical" href="https://proximity-tools.com/[tool-name].html">
```

### JSON-LD Schema Template
```json
{
  "@context": "https://schema.org",
  "@type": "WebApplication",
  "name": "[Tool Name]",
  "description": "[Tool description]",
  "url": "https://proximity-tools.com/[tool-name].html",
  "applicationCategory": "DeveloperApplication",
  "operatingSystem": "Web Browser"
}
```

**Important:** Always replace `[tool-name]` with the actual tool filename and update all bracketed placeholders with appropriate content. 
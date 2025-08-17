# Node.js Runner - VS Code Extension

A powerful Visual Studio Code extension for executing JavaScript and TypeScript files with a simple play button and integrated console output.

## ✨ Features

### 🎯 Core Functionality
- **▶️ One-Click Execution**: Play button directly in the editor toolbar
- **📊 Integrated Console**: All output displayed directly in VS Code
- **🔄 Real-time Output**: Live streaming of program output
- **⚡ Smart Detection**: Automatic recognition of `.js` and `.ts` files
- **🎛️ Flexible**: Execute current file or `app.js`
- **📋 Side Panel**: Dedicated panel with file explorer and quick actions

### 🛠️ Advanced Features
- **⌨️ Keyboard Shortcuts**: 
  - `Ctrl+F5`: Execute current file
  - `Ctrl+Shift+F5`: Execute app.js
  - `Ctrl+Shift+N`: Open Node.js Runner panel
  - `Ctrl+Shift+X`: Stop running process
- **🎨 Status Bar Integration**: Live status and quick access
- **🛑 Process Control**: Stop running processes
- **🧹 Output Management**: Clear and manage output
- **⚙️ Configurable**: Customizable Node.js settings
- **🌐 Multi-language**: English and German interface

### 📋 Side Panel
- **📁 File Explorer**: Browse all JavaScript/TypeScript files in workspace
- **⚡ Quick Actions**: One-click access to all commands
- **⚙️ Settings**: View and modify extension settings
- **🔄 Auto-refresh**: Automatically updates when files change

## 🚀 Quick Start

1. **Installation**: Install the extension from VS Code Marketplace
2. **Open File**: Open a `.js` or `.ts` file
3. **Execute**: Click the ▶️ play button in the toolbar or use `Ctrl+F5`
4. **View Output**: See results in the "Node.js Runner" output channel
5. **Panel Access**: Click the Node.js Runner icon in the activity bar

## 📋 Usage

### Play Button Options

| Action | Shortcut | Description |
|--------|----------|-------------|
| **Run Current File** | `Ctrl+F5` | Executes the currently opened file |
| **Run app.js** | `Ctrl+Shift+F5` | Executes app.js from workspace root |
| **Stop Running** | `Ctrl+Shift+X` | Stops the running process |
| **Clear Output** | - | Clears the console |
| **Open Panel** | `Ctrl+Shift+N` | Opens the Node.js Runner side panel |

### Supported File Types

- ✅ **JavaScript** (`.js`) - Direct execution with Node.js
- ✅ **TypeScript** (`.ts`) - Automatic compilation with ts-node

### Context Menu Integration

Right-click on JavaScript/TypeScript files for quick access:
- ▶️ Run Node.js File
- ▶️ Run app.js

## ⚙️ Configuration

Go to VS Code Settings and search for "Node.js Runner":

```json
{
  "nodejs-runner.nodeExecutable": "node",
  "nodejs-runner.clearOutputBeforeRun": true,
  "nodejs-runner.showRunningIndicator": true,
  "nodejs-runner.autoSaveBeforeRun": true,
  "nodejs-runner.nodeArguments": [],
  "nodejs-runner.language": "en"
}
```

### Language Settings
- **English**: `"nodejs-runner.language": "en"` (default)
- **German**: `"nodejs-runner.language": "de"`

### Advanced Node.js Arguments

```json
{
  "nodejs-runner.nodeArguments": [
    "--experimental-modules",
    "--max-old-space-size=4096"
  ]
}
```

## 🎯 Examples

### Example app.js
```javascript
console.log('🚀 Hello from app.js!');
console.log('📅 Current time:', new Date().toLocaleString());

setTimeout(() => {
    console.log('✅ Processing completed!');
    console.log('- Version:', process.version);
    console.log('- Platform:', process.platform);
}, 1000);
```

### Example TypeScript
```typescript
interface User {
    name: string;
    age: number;
}

const user: User = {
    name: 'John Doe',
    age: 30
};

console.log('👤 User:', user);
console.log('🎉 TypeScript is running perfectly!');
```

## 🔧 TypeScript Support

For TypeScript files you need `ts-node`:

```bash
# Global installation
npm install -g ts-node

# Or project-local
npm install ts-node --save-dev
```

The extension automatically tries:
1. `ts-node` (globally installed)
2. `npx ts-node` (project-local)

## 📊 Output Channel Features

### Formatted Output
- 🔄 **Status Indicators**: Clearly recognizable symbols
- 📁 **Path Display**: Complete file path
- ⚙️ **Configuration**: Node.js version and arguments
- ✅/❌ **Exit Codes**: Success/error status

### Example Output
```
🔄 Running: app.js
📁 Path: C:\\workspace\\app.js
⚙️ Node: node
--------------------------------------------------
🚀 Hello from app.js!
📅 Current time: 8/17/2025, 3:30:45 PM
✅ Processing completed!
--------------------------------------------------
✅ Process completed successfully (exit code: 0)
```

## 🚦 Status Bar Integration

The status bar shows:
- **$(play) Run JS**: Ready to execute
- **$(debug-stop) Stop JS**: Process running (click to stop)

## 🛠️ Development

### Test Extension Locally

1. Clone repository
2. Install dependencies: `npm install`
3. Compile: `npm run compile`
4. Press F5 for development host
5. Test extension in new VS Code window

### Scripts

```bash
npm run compile         # Compile TypeScript
npm run watch          # Watch mode for development
npm run package        # Production build
npm run lint           # Run ESLint
npm run test           # Run tests
```

## 📂 Project Structure

```
node-js-engine/
├── src/
│   ├── extension.ts        # Main extension code
│   ├── panels.ts          # Side panel providers
│   ├── i18n/              # Internationalization
│   │   ├── index.ts       # I18n manager
│   │   ├── en.ts          # English translations
│   │   └── de.ts          # German translations
│   └── test/              # Tests
├── resources/
│   └── icon.svg           # Extension icon
├── package.json           # Extension manifest
├── tsconfig.json          # TypeScript config
├── webpack.config.js      # Webpack config
└── README.md              # This file
```

## 🐛 Troubleshooting

### Node.js Not Found
```bash
# Install Node.js or configure path
"nodejs-runner.nodeExecutable": "C:\\Program Files\\nodejs\\node.exe"
```

### TypeScript Errors
```bash
# Install ts-node
npm install -g ts-node
```

### Permission Errors (Linux/Mac)
```bash
# Node.js executable permissions
chmod +x /usr/local/bin/node
```

## 🤝 Contributing

1. Fork the repository
2. Create feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open pull request

## 📄 License

MIT License

## 📧 Contact & Support

- **Website**: [pyengine.de](https://pyengine.de)
- **Email**: admin@pyengine.de
- **Bug Tracker**: [bug.pyengine.de/program/5](https://bug.pyengine.de/program/5)
- **Support**: Create an issue on GitHub

## 🎉 Changelog

### 0.0.1 (Current)
- ✨ Initial Release
- ▶️ Play Button Integration
- 📊 Output Channel Support
- ⌨️ Keyboard Shortcuts
- ⚙️ Configuration Options
- 🔄 Process Management
- 🎯 TypeScript Support
- 📋 Side Panel Integration
- 🌐 Multi-language Support (EN/DE)

## 💡 Roadmap

- [ ] 🔧 Environment Variables Support
- [ ] 📦 NPM Script Integration  
- [ ] 🧪 Testing Framework Integration
- [ ] 🔍 Debugging Support
- [ ] 📈 Performance Monitoring
- [ ] 🌐 Remote Execution

---

**Copyright © 2025 [pyengine.de](https://pyengine.de) - All rights reserved**

*Developed with ❤️ for the VS Code Community*

*Feedback and feature requests are welcome! Create an issue on GitHub.*

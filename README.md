# QtNovaFramelessSubwindow

**QtNovaFramelessSubwindow** is a reusable Qt widget that acts as a **frameless subwindow**. It provides a custom **title bar**, **close button**, and supports **dark mode** for modern styled UIs.

## ✨ Features
- Frameless child window (no native OS frame).
- Custom title bar with close and minimize button.
- Dark mode and themed icon support.
- Extend content into titlebar without facing any difficulty

## Screenshot
<img width="1592" height="847" alt="Screenshot (100)" src="https://github.com/user-attachments/assets/d205e38a-0ebe-4190-a154-84e081ad40a1" />

## 🚀 Usage

### Include in your project
1. Copy `SubWindow.h` and `SubWindow.cpp` into your project’s `src/` folder.
2. Include the header in your code:

```cpp
#include "SubWindow.h"
SubWindow *sub = new SubWindow(1000, 720, parentWidget);
sub->show();
```
### How to Add Custom widgets to SubWindow

```cpp
// Create a SubWindow
SubWindow *sub = new SubWindow(parentWidget);
sub->setGeometry(100, 100, 600, 400);

// Add your custom widget
QLabel *label = new QLabel("Hello from SubWindow!");
QPushButton *btn = new QPushButton("Click Me");

// Optionally arrange them with a layout inside content area
QVBoxLayout *layout = new QVBoxLayout(sub->contentArea());
layout->addWidget(label);
layout->addWidget(btn);

sub->show();
```
> [!NOTE]
> If you want to enable close or minimze button in the titlebar of subwindow, then you must pass true value to the constructor of subwindow. You can disable both buttons by passing False to the constructor.

> [!IMPORTANT]
> Before using this SubWindow in your project, make sure the `correct paths` to `Custom Button and ToolTip UI Component` are placed in `CMakeLists.txt` and also in `SubWindow.h` to work efficiently.

# 视频音频分离工具

## 简介
视频音频分离工具是一款基于 Python 和 FFmpeg 的桌面应用程序，支持从视频文件中分离音频流或视频流。通过简洁美观的图形界面，用户只需简单操作即可完成处理，支持文件拖拽功能，更加方便快捷。

---

## 功能特点
- **音频提取**：从视频文件中提取音频，支持保存为 MP3、WAV、AAC 等格式。
- **视频提取**：从视频文件中分离视频流，去除音频部分，支持 MP4、MKV、AVI 等格式。
- **文件拖拽支持**：可直接将视频文件拖拽到工具窗口，快速识别文件。
- **实时进度显示**：处理过程中显示分离进度。
- **简单易用**：图形界面直观，适合非技术用户使用。

---

## 使用方法

1. **运行程序**
   下载并运行打包好的 `.exe` 文件，或者使用 Python 脚本直接运行。

2. **选择文件**
   - 点击“浏览”按钮，选择视频文件。
   - 或直接将视频文件拖拽到窗口。

3. **设置输出选项**
   - 选择需要分离的内容（音频或视频）。
   - 指定目标文件格式：
     - 音频：MP3、WAV、AAC。
     - 视频：MP4、MKV、AVI。

4. **开始处理**
   点击“开始分离”，等待处理完成，工具会提示保存的文件路径。

---

## 系统要求
- **操作系统**：Windows 10 或更高版本
- **运行环境**：Python 3.7 或更高版本
- **必备组件**：
  - FFmpeg（需添加到系统环境变量）
  - 依赖库：
    - tkinter
    - tkinterdnd2
    - ttkthemes

---

## 安装与运行

### 运行 Python 脚本
1. 安装依赖：
   ```bash
   pip install tkinterdnd2 ttkthemes
   ```
2. 确保 FFmpeg 已安装并配置到环境变量。
3. 执行脚本：
   ```bash
   python video_separator.py
   ```

### 打包为可执行文件
1. 安装打包工具：
   ```bash
   pip install pyinstaller
   ```
2. 执行以下命令进行打包：
   ```bash
   pyinstaller --onefile --windowed --add-data "path_to_tkinterdnd2;tkinterdnd2" --icon=app_icon.ico video_separator.py
   ```
3. 打包完成后，生成的 `.exe` 文件在 `dist` 文件夹中。

---



---

## 常见问题

### 1. 程序无法运行？
- 请确认已安装 FFmpeg 并正确配置到环境变量。
- 如果使用源代码运行，确保已安装所有依赖库。

### 2. 拖拽功能不起作用？
拖拽功能依赖 `tkinterdnd2` 模块，确保其已安装并在打包时正确包含。

### 3. 输出格式不符合预期？
确认在操作前正确选择了目标格式和分离类型。

---

## 开发者信息

- **作者**：Leo Zivika  
- **GitHub 开源地址**：[视频音频分离工具](https://github.com/147258-gif/video_separator_with_drag_drop)

---

## 许可证
本项目基于 MIT 许可证开源，详细内容请参阅 [LICENSE](LICENSE) 文件。
```


# Hướng dẫn sử dụng

Báo cáo môn **Phương pháp số cho Đại số tuyến tính** — Nguyễn Hồ Bảo Thiên, Khoa học dữ liệu K28B, Trường Đại học Quy Nhơn.

---

## Cấu trúc thư mục

```
.
├── REPORT.pdf              # File báo cáo hoàn chỉnh (đã compile)
├── Resource/
│   ├── Report_TeX.tex      # Mã nguồn LaTeX của báo cáo
│   └── qnu_logo.jpg        # Logo Trường Đại học Quy Nhơn (dùng trong trang bìa)
├── Scripts/
│   └── PP_số_cho_ĐSTT.ipynb  # Notebook Python minh họa các thuật toán
└── tmp/
    └── README.md           # File này
```

---

## Build file PDF từ file `.tex` trên Visual Studio Code

### Yêu cầu

- Cài **TeX distribution**: [MiKTeX](https://miktex.org/) (Windows) hoặc [TeX Live](https://tug.org/texlive/) (Linux/macOS).
- Cài extension **LaTeX Workshop** trên VS Code (tìm trong Extensions: `James-Yu.latex-workshop`).

### Các bước thực hiện

1. Mở thư mục dự án trong VS Code.
2. Mở file `Resource/Report_TeX.tex`.
3. Build bằng một trong hai cách:
   - Nhấn `Ctrl + Alt + B` để build.
   - Hoặc click biểu tượng **▶ Build LaTeX project** ở góc trên phải.
4. File `REPORT.pdf` sẽ được tạo ra sau khi build thành công.

> **Lưu ý:** File `.tex` dùng engine **XeLaTeX** (khai báo ở dòng đầu `% !TeX program = xelatex`). LaTeX Workshop sẽ tự động dùng đúng engine này.

> Các file tạm sinh ra trong quá trình build (`.aux`, `.toc`, `.out`, `.log`, ...) có thể xóa tự do mà không ảnh hưởng đến kết quả — LaTeX sẽ tự tạo lại khi build lần tiếp theo.

---

## Chạy file `.ipynb` trên VS Code hoặc Google Colab

### Cách 1 — VS Code

**Yêu cầu:**
- Cài extension **Jupyter** trên VS Code (`ms-toolsai.jupyter`).
- Cài Python và các thư viện cần thiết:
  ```bash
  pip install numpy scipy matplotlib
  ```

**Các bước:**
1. Mở file `Scripts/PP_số_cho_ĐSTT.ipynb` trong VS Code.
2. Chọn Python kernel ở góc trên phải (thường là môi trường Python đang dùng).
3. Nhấn **Run All** (hoặc `Shift + Enter` để chạy từng cell).

---

### Cách 2 — Google Colab

1. Truy cập [colab.research.google.com](https://colab.research.google.com).
2. Chọn **File → Upload notebook**.
3. Upload file `Scripts/PP_số_cho_ĐSTT.ipynb`.
4. Chạy từng cell hoặc nhấn **Runtime → Run all**.

> Các thư viện `numpy`, `scipy`, `matplotlib` đã được cài sẵn trên Google Colab, không cần cài thêm.

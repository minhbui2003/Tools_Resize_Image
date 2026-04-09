# POD Resize Tool

Tool resize ảnh hàng loạt dành cho POD (Print-on-Demand)\
Hỗ trợ scale theo tỉ lệ hoặc resize theo kích thước cụ thể, giữ nguyên
cấu trúc folder.

------------------------------------------------------------------------

## 1. Cài đặt

### Yêu cầu

-   Python 3.8+

### Thư viện

``` bash
pip install Pillow
```

------------------------------------------------------------------------

## 2. Cách chạy tool

``` bash
python resize.py
```

------------------------------------------------------------------------

## 3. Chức năng

1.  Chọn thư mục nguồn\
2.  Chọn thư mục xuất\
3.  Chọn kích thước ảnh\
4.  Định dạng ảnh xuất\
5.  Log & Progress

------------------------------------------------------------------------

## 4. Cách hoạt động

Tool sẽ:

-   Scan toàn bộ ảnh trong folder nguồn\
-   Giữ nguyên cấu trúc thư mục\
-   Resize từng ảnh\
-   Lưu vào folder mới:

``` bash
[source_folder]_scaled/
```

------------------------------------------------------------------------

## 5. Logic xử lý ảnh

-   Dùng Pillow (`Image.resize`)\
-   Filter: `LANCZOS` (chất lượng cao)\
-   DPI: `300`\
-   JPG sẽ auto convert RGB nếu có alpha

------------------------------------------------------------------------

## 6. Build file .exe (tuỳ chọn)

Bạn có thể build thành file chạy trực tiếp:

``` bash
pip install pyinstaller
pyinstaller --onefile --windowed resize.py
```

File exe nằm trong:

``` bash
dist/
```

------------------------------------------------------------------------

## 7. Tác giả

Minh (POD Software)

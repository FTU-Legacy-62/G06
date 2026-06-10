# PricePilot

## Mã nhóm

G06

## Thành viên

| Họ tên         | Mã sinh viên | Vai trò chính                                                          |
| -------------- | ------------ | ---------------------------------------------------------------------- |
| Đỗ Thị Quỳnh Anh | 2313380004       | Economic Logic & Pricing Model   |
| Trần Hà Dương | 2312380005 | Data & Input  |
| Nguyễn Mai Anh | 2313380002 | Monte Carlo Simulation |
| Đàm Ngọc Hà Phương      | 2313380028 | Advisory Logic & Strategy Engine|
| Nông Đức Minh | 2312380020       | Web & Result Display |

## Mô tả ngắn về sản phẩm

PricePilot là một web app hỗ trợ doanh nghiệp cơ khí vừa và nhỏ đánh giá tác động của việc tăng giá bán. Người dùng có thể nhập dữ liệu chi phí sản xuất, số lượng đơn hàng hiện tại, dữ liệu giá bán và demand trong quá khứ, sau đó hệ thống sẽ mô phỏng nhiều mức tăng giá khác nhau. Sản phẩm sử dụng historical price elasticity để ước tính phản ứng của khách hàng khi giá thay đổi và dùng Monte Carlo simulation để xét các yếu tố thị trường bất định. Kết quả trả về là một dashboard gồm profit, demand, downside risk và ba chiến lược giá: Aggressive, Balanced, Conservative. Mục tiêu của sản phẩm là giúp doanh nghiệp đưa ra quyết định tăng giá có cơ sở hơn thay vì chỉ dựa vào cảm tính.

## Vấn đề sản phẩm giải quyết

Trong bối cảnh giá nguyên vật liệu đầu vào biến động, các doanh nghiệp cơ khí SME thường gặp khó khăn khi quyết định có nên tăng giá bán hay không. Nếu tăng giá quá thấp, doanh nghiệp có thể không cải thiện được lợi nhuận. Nếu tăng giá quá cao, khách hàng có thể giảm đơn hàng, trì hoãn đơn hàng hoặc chuyển sang nhà cung cấp khác.

Vấn đề này đặc biệt quan trọng vì quyết định giá bán ảnh hưởng trực tiếp đến lợi nhuận, số lượng đơn hàng, khả năng giữ chân khách hàng và năng lực cạnh tranh của doanh nghiệp. Trong thực tế, nhiều doanh nghiệp nhỏ chưa có công cụ định lượng đơn giản để so sánh giữa lợi nhuận tăng thêm và rủi ro mất demand.

PricePilot giải quyết vấn đề này bằng cách biến quyết định tăng giá thành một mô hình mô phỏng có input, công thức xử lý, kết quả dashboard và recommendation rõ ràng. Người dùng có thể thử nhiều kịch bản khác nhau trước khi đưa ra quyết định kinh doanh.

## Người dùng mục tiêu

Người dùng chính của sản phẩm là: các doanh nghiệp vừa và nhỏ về lĩnh vực gia công cơ khí

Người dùng sử dụng sản phẩm khi muốn kiểm tra một mức tăng giá có hợp lý hay không, hoặc khi muốn so sánh nhiều kịch bản tăng giá trong điều kiện thị trường bất định.

## Tính năng chính

- Tính toán cost structure, cost per order, base price và current profit của doanh nghiệp.
- Ước tính historical price elasticity từ dữ liệu giá bán và demand trong quá khứ.
- Áp dụng Monte Carlo simulation để mô phỏng profit, demand và risk ở nhiều mức tăng giá khác nhau.
- So sánh các kịch bản tăng giá và đề xuất ba chiến lược: Aggressive, Balanced và Conservative.
- Hiển thị dashboard kết quả gồm expected profit, demand loss, downside risk, biểu đồ phân tích và Monte Carlo Profit Distribution.
- Tạo recommendation và Personalized Detailed Insight dựa trên input và kết quả mô phỏng của từng doanh nghiệp.

## Cách mở hoặc chạy sản phẩm

Có hai cách để mở hoặc chạy sản phẩm:

1. Mở trực tiếp bằng link demo.
2. Chạy local trên máy tính bằng Python.


## Cách 1: Mở bằng link demo

1. Mở link demo của sản phẩm:

```text
https://pricepilot123.onrender.com/
```

2. Web được deploy bằng Render free service, lần mở đầu có thể mất khoảng 30–60 giây do server cần khởi động lại.
3. Khi trang intro của PricePilot hiện ra, bấm **Start**.
4. Ở trang input, khách hàng nhập dữ liệu input mong muốn.
5. Điều chỉnh các thông số:

   * material type;
   * tons per month;
   * waste rate;
   * labor cost;
   * fixed cost;
   * base demand;
   * target margin;
   * historical price-demand data;
   * market uncertainty ranges;
   * số lần Monte Carlo simulations.
6. Bấm **Run Simulation**.
7. Trang loading sẽ hiển thị tiến trình chạy simulation.
8. Sau khi quá trình tính toán hoàn tất, hệ thống tự chuyển sang trang result.
9. Ở trang result, người dùng có thể xem:

   * recommended price increase range;
   * expected profit;
   * probability of lower profit;
   * average demand;
   * average demand loss;
   * các biểu đồ phân tích;
   * ba strategy: Aggressive, Balanced, Conservative;
   * personalized detailed insight.
10. Có thể bấm **Run again** hoặc **Try Again** để quay lại trang input và chạy lại với assumptions khác.

---

## Cách 2: Chạy local trên máy tính

Nếu không dùng link demo online, người dùng có thể tải repo về máy và chạy trực tiếp bằng Python.

1. Tải code từ GitHub 

Vào repo nhóm G06 trên GitHub, bấm nút **Code**, chọn **Download ZIP**, sau đó giải nén file ZIP vào một thư mục trên máy. Ví dụ có thể giải nén vào thư mục `C:\Users\YourName\Desktop\G06`.

Nếu dùng Git, có thể chạy lệnh `git clone https://github.com/FTU-Legacy-62/G06.git`, sau đó vào thư mục project bằng lệnh `cd G06`.

2. Kiểm tra Python

Mở Command Prompt hoặc Terminal và chạy lệnh `python --version`. Nếu dùng Windows mà lệnh này không chạy, có thể thử `py --version`.

Nếu máy chưa có Python, cần cài Python 3 trước. Khi cài Python trên Windows, nên chọn mục **Add Python to PATH** để có thể chạy Python từ Command Prompt.

3. Kiểm tra các file trong repo

Sau khi tải repo về máy, thư mục project cần có các file chính như `pricepilot.py`, `requirements.txt`, `README.md`, `GROUP_FOOTPRINT.md` và `INDIVIDUAL_FOOTPRINT.md`.

Trong đó, `pricepilot.py` là file chính để chạy web app. File `requirements.txt` là file liệt kê các thư viện Python cần thiết để app hoạt động.

4. Cài thư viện cần thiết

Trong thư mục chứa file `pricepilot.py`, chạy lệnh `pip install -r requirements.txt` để cài thư viện.

Nếu Windows không nhận lệnh `pip`, có thể dùng lệnh `py -m pip install -r requirements.txt`.

Các thư viện chính trong `requirements.txt` gồm Flask, pandas, numpy, plotly và gunicorn. Flask dùng để tạo web app, pandas và numpy dùng để xử lý dữ liệu và tính toán simulation, plotly dùng để hiển thị biểu đồ, còn gunicorn dùng khi deploy app lên Render.

5. Chạy ứng dụng

Sau khi cài xong thư viện, chạy app bằng lệnh `python pricepilot.py`. Nếu dùng Windows và lệnh `python` không chạy, có thể dùng `py pricepilot.py`.

Khi chạy thành công, terminal sẽ hiện đường link local, thường là `http://127.0.0.1:5000`.

6. Mở app trên trình duyệt

Mở Chrome, Edge hoặc trình duyệt bất kỳ, sau đó truy cập `http://127.0.0.1:5000`.

Sau khi mở được app, demo theo thứ tự: mở trang intro, bấm **Start**, nhập dữ liệu hoặc giữ dữ liệu mẫu ở trang input, chọn số lần Monte Carlo simulations, bấm **Run Simulation**, chờ trang loading chạy xong và xem trang result.

Ở trang result, người dùng có thể xem recommended price range, expected profit, demand loss, downside risk, các biểu đồ phân tích, Monte Carlo Profit Distribution và phần Personalized Detailed Insight.
## Cách chạy nếu gặp lỗi thường gặp

### Lỗi 1: Thiếu thư viện

Nếu gặp lỗi dạng:

```text
ModuleNotFoundError: No module named 'flask'
```

hoặc:

```text
ModuleNotFoundError: No module named 'pandas'
```

thì chạy lại:

```bash
pip install -r requirements.txt
```

hoặc:

```bash
py -m pip install -r requirements.txt
```

---

### Lỗi 2: Không mở được `127.0.0.1:5000`

Kiểm tra terminal xem Flask app còn đang chạy không. Nếu terminal đã bị đóng, chạy lại:

```bash
python pricepilot.py
```

hoặc đúng tên file Python chính của nhóm.

Sau đó mở lại:

```text
http://127.0.0.1:5000
```

---

### Lỗi 3: Port 5000 đang bị dùng

Nếu port 5000 đang bị dùng bởi một app khác, hãy tắt terminal cũ đang chạy Flask app rồi chạy lại.

---



## Ghi chú về dữ liệu nếu có

Sản phẩm sử dụng dữ liệu do người dùng nhập và dữ liệu giả lập phục vụ mục đích demo. Các dữ liệu mẫu trong app như chi phí nguyên vật liệu, số lượng đơn hàng, target margin, historical price-demand data và market uncertainty ranges được dùng để minh họa cách mô hình hoạt động.

Các biến thị trường như market growth, customer budget pressure, material shock impact và material inflation được nhập dưới dạng range để phục vụ Monte Carlo simulation. Đây là các giả định mô phỏng, không phải dự báo chắc chắn.

Repo không chứa dữ liệu cá nhân, API key, mật khẩu, token hoặc dữ liệu nội bộ của doanh nghiệp.

## Ghi chú thêm

README là trang giới thiệu nhanh sản phẩm và hướng dẫn người khác mở hoặc chạy app. Phần giải thích chi tiết hơn về logic sản phẩm, công thức xử lý, lựa chọn mô hình, recommendation engine, hạn chế và bài học được trình bày trong file:

```text
GROUP_FOOTPRINT.md
```

Đóng góp cụ thể của từng thành viên được trình bày trong file:

```text
INDIVIDUAL_FOOTPRINT.md
```

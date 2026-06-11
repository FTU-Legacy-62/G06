**Individual Footprint**

**Họ và tên:**
**Nông Đức Minh**

**Mã sinh viên:**
**2312380020**

## Vai trò trong dự án

Trong dự án PricePilot, em phụ trách chính phần **M5 – Web & Result Display**. Đây là phần liên quan đến giao diện web, cách trình bày kết quả mô phỏng và trải nghiệm người dùng khi sử dụng sản phẩm.

Cụ thể, phần việc của em tập trung vào việc biến các kết quả tính toán từ mô hình mô phỏng Monte Carlo và advisory logic thành một dashboard dễ hiểu, trực quan và có thể dùng để demo. Em không chỉ làm phần hiển thị số liệu, mà còn sắp xếp lại thông tin theo một luồng hợp lý để người dùng có thể hiểu được: nên tăng giá bao nhiêu, lợi nhuận thay đổi thế nào, rủi ro ra sao và nhu cầu có thể bị ảnh hưởng như thế nào.

Các phần em phụ trách bao gồm giao diện trang giới thiệu, trang nhập liệu, trang loading, trang kết quả, các KPI cards, biểu đồ, scenario recommendation cards, phần Monte Carlo Profit Distribution và phần Personalized Detailed Insight.


## Dấu ấn cá nhân trong sản phẩm

Dấu ấn cá nhân rõ nhất của em nằm ở trang **PricePilot Result Dashboard**. Đây là trang kết quả cuối cùng sau khi người dùng nhập dữ liệu và chạy mô phỏng.

Khi làm phần này, em tập trung vào việc biến kết quả mô phỏng thành một dashboard dễ đọc và dễ ra quyết định. Phần đầu trang hiển thị ngay recommendation chính, gồm mức tăng giá được khuyến nghị, lợi nhuận kỳ vọng, mức thay đổi lợi nhuận, xác suất lợi nhuận thấp hơn hiện tại và mức mất nhu cầu trung bình.

Bên dưới, em xây dựng hệ thống KPI cards hiển thị các thông số output cần thiết, hai biểu đồ **Profit vs. Price Increase** và **Demand vs. Price Increase**, cùng phần so sánh ba chiến lược **Aggressive, Balanced và Conservative**. Em cũng trình bày lại phần **Monte Carlo Profit Distribution** dưới dạng một tab có thể pop-up tương tác, cho phép người dùng chọn từng mức tăng giá và xem các trường hợp có thể xảy ra. Ngoài ra, em chỉnh các phần, **Personalized Detailed Insight**  để kết quả có giải thích rõ ràng hơn. Đặc biệt, khi profit improvement âm, em sửa cách hiển thị thành **Defensive Recommendation** để tránh gây hiểu nhầm rằng hệ thống đang khuyến nghị tăng giá như một cơ hội tăng lợi nhuận. Trong trường hợp đó, recommendation được hiểu là phương án phòng thủ phù hợp hơn dưới các giả định hiện tại.

Nhìn chung, đóng góp chính của em là xây dựng giao diện kết quả hoàn chỉnh, trực quan và đủ rõ để người dùng hiểu được recommendation cũng như demo sản phẩm thuyết phục hơn.


## Những việc đã thực sự làm

Trong quá trình làm dự án, em đã thực hiện các phần sau:

* Thiết kế và xây dựng giao diện chính của web PricePilot, bao gồm intro page, input page, loading page và result page.
* Xây dựng dashboard kết quả với các KPI chính như current base price, current expected profit, recommended range, expected profit, best single increase, downside risk và demand loss.
* Thiết kế phần recommendation chính ở đầu trang kết quả để người dùng nhìn vào là thấy ngay mức tăng giá được hệ thống đề xuất.
* Xây dựng ba scenario cards gồm Aggressive, Balanced và Conservative để so sánh các lựa chọn chiến lược.
* Tạo biểu đồ **Profit vs. Price Increase** để thể hiện lợi nhuận kỳ vọng theo từng mức tăng giá.
* Tạo biểu đồ **Demand vs. Price Increase** để thể hiện tác động của tăng giá lên nhu cầu trung bình.
* Xây dựng tab **Monte Carlo Profit Distribution** để người dùng xem phân phối lợi nhuận tại từng mức price increase.
* Thiết kế phần **Quick Personalized Insights** để tóm tắt nhanh các điểm quan trọng của kết quả.
* Xây dựng khu vực hiển thị **Personalized Detailed Insight**, cho phép người dùng bấm để mở phần phân tích chi tiết.
* Chỉnh logic hiển thị khi profit improvement âm, chuyển từ cách nói “profit improvement” sang hướng “defensive adjustment” hoặc “profit gap vs current” cho hợp lý hơn.
* Thêm các nút điều hướng như Run Again, Try Again, Download Report và View Full Personalized Analysis.
* Chỉnh CSS, màu sắc, spacing, layout, hover effect và responsive design để giao diện nhìn rõ ràng hơn khi demo.
* Chỉnh loading page để quá trình chạy simulation mượt hơn, tránh việc vừa bấm chạy đã nhảy ngay sang trang kết quả.


## File, tính năng, giao diện hoặc phần demo đã đóng góp

Phần em đóng góp nằm chủ yếu trong file **pricepilot.py**, đặc biệt là các phần giao diện và hiển thị kết quả.

### 1. RESULT_HTML – Result Dashboard

Trong dự án, em tập trung nhiều vào phần **Result Dashboard** vì đây là màn hình tổng hợp kết quả sau khi người dùng hoàn thành bước nhập dữ liệu và chạy mô phỏng. Thay vì để kết quả xuất hiện dưới dạng nhiều con số rời rạc, em sắp xếp lại thành một dashboard có bố cục rõ ràng hơn. Trên dashboard có phần khuyến nghị chính, các KPI quan trọng, biểu đồ, phần so sánh scenario và phần insight giải thích kết quả.

Cách trình bày này giúp người dùng theo dõi kết quả dễ hơn. Khi nhìn vào trang result, người dùng có thể nhanh chóng biết hệ thống đang đề xuất mức tăng giá nào, lợi nhuận kỳ vọng thay đổi ra sao, rủi ro nằm ở đâu và nhu cầu có thể bị ảnh hưởng như thế nào.

### 2. Top Recommendation Section

Em thiết kế phần khuyến nghị chính ở đầu dashboard để người dùng vừa mở trang kết quả là thấy ngay kết luận quan trọng nhất.

Phần này hiển thị các thông tin như:

- Recommended range.
- Recommended single increase.
- Expected profit.
- Profit improvement hoặc profit gap.
- Probability of lower profit.
- Average demand loss.

Trong quá trình kiểm thử, em nhận ra có trường hợp mô hình không tìm được kịch bản thật sự tạo ra lợi nhuận tốt hơn hiện tại. Nếu vẫn hiển thị theo kiểu “profit opportunity” thì sẽ dễ gây hiểu nhầm cho người dùng.

Vì vậy, em chỉnh lại phần này theo hướng trung thực hơn: khi profit improvement âm, dashboard sẽ chuyển sang dạng **Defensive Recommendation**, ví dụ như “Increase price by X%” nhưng kèm thông báo rằng không có kịch bản nào hoàn toàn có lợi nhuận cao hơn dưới các giả định hiện tại.

Cách sửa này giúp dashboard không chỉ đẹp hơn mà còn hợp lý hơn về mặt giải thích. Người dùng có thể hiểu rằng recommendation trong trường hợp đó không phải là cơ hội tăng lợi nhuận mạnh, mà là lựa chọn phòng thủ tốt nhất trong điều kiện đầu vào hiện tại.

### 3. KPI Cards

Em xây dựng các KPI cards để tóm tắt những chỉ số quan trọng nhất của kết quả mô phỏng. Thay vì để người dùng phải đọc nhiều dòng số liệu hoặc bảng kết quả dài, em đưa các chỉ số chính thành từng ô riêng biệt trên dashboard.

Các KPI này bao gồm current base price, current expected profit, recommended range, expected profit, best single increase, profit improvement, probability of lower profit, average demand, average demand loss và số lần simulation.

Phần KPI cards giúp người dùng nắm nhanh tình hình tổng quan của doanh nghiệp sau khi chạy mô phỏng. Ví dụ, người dùng có thể nhìn ngay doanh nghiệp đang có lợi nhuận hiện tại bao nhiêu, mức tăng giá được đề xuất là bao nhiêu, lợi nhuận kỳ vọng thay đổi thế nào và rủi ro giảm lợi nhuận có cao không.

Em cũng chỉnh cách đặt label, cách chia card và cách hiển thị số liệu để dashboard dễ đọc hơn khi demo.

### 4. Profit vs. Price Increase Chart

Em trình bày biểu đồ lợi nhuận kỳ vọng theo từng mức tăng giá. Biểu đồ này giúp người dùng thấy mức tăng giá nào tạo expected profit cao hơn, thay vì chỉ nhìn một con số recommendation.

### 5. Demand vs. Price Increase Chart

Em trình bày biểu đồ nhu cầu trung bình theo từng mức tăng giá. Đây là phần quan trọng vì tăng giá không chỉ ảnh hưởng đến profit mà còn có thể làm giảm số lượng đơn hàng.

### 6. Monte Carlo Profit Distribution Tab

Em xây dựng phần tab có thể pop-up để người dùng chọn từng mức price increase và xem phân phối lợi nhuận tương ứng. Phần này giúp kết quả Monte Carlo dễ hiểu hơn, vì người dùng có thể thấy expected profit, lower profit probability và average demand tại từng mức giá.

### 7. Scenario Recommendation Cards

Em thiết kế ba thẻ so sánh chiến lược:

* Aggressive.
* Balanced.
* Conservative.

Mỗi thẻ có expected profit, profit improvement hoặc profit gap, risk, demand loss và đoạn thông tin chú thích riêng. Sau khi kiểm tra các trường hợp profit âm, em chỉnh lại để tên scenario vẫn giữ nguyên, nhưng label “Profit improvement” sẽ đổi thành “Profit gap vs current” nếu số đó âm.

### 8. Quick Personalized Insights

Em xây dựng phần insight ngắn để tóm tắt nhanh ba điểm chính: profit, risk và demand impact. Khi profit improvement âm, em chỉnh lại title và nội dung để không còn câu kiểu “improves expected profit by -33%”, mà chuyển sang cách giải thích đây là defensive adjustment.

### 9. Personalized Detailed Insight Display

Em xây dựng khu vực hiển thị phần phân tích chi tiết cá nhân hóa. Người dùng có thể bấm **View Full Personalized Analysis** để mở hoặc đóng phần này. Phần này giúp dashboard không bị quá dài ngay từ đầu, nhưng vẫn có đủ giải thích khi cần.

### 10. CSS, layout và responsive design

Em chỉnh bố cục dashboard theo dạng card layout, dùng grid, spacing, màu sắc và hover effect để giao diện nhìn gọn hơn. Em cũng chỉnh responsive design để giao diện vẫn dùng được trên các kích thước màn hình khác nhau.

### 11. Loading screen

Em xây dựng và chỉnh loading screen khi hệ thống chạy simulation. Trang này có progress bar, status text, estimated time remaining

## Bằng chứng đóng góp

Các bằng chứng đóng góp của em tập trung vào phần giao diện web, luồng demo và trang hiển thị kết quả của PricePilot.

* File chính: **pricepilot.py**
* Link web demo: **https://pricepiloot.onrender.com/**

### 1. Trang Intro


<img width="1894" height="858" alt="Screenshot (3287)" src="https://github.com/user-attachments/assets/c0593722-3c6d-4543-b3e5-8461b5a78cf0" />


Trang intro là màn hình đầu tiên của sản phẩm. Phần này giới thiệu ngắn gọn PricePilot, giải thích sản phẩm hỗ trợ quyết định định giá cho doanh nghiệp sản xuất cơ khí và có nút để người dùng bắt đầu nhập dữ liệu.

### 2. Trang Input


<img width="1834" height="864" alt="Screenshot (3288)" src="https://github.com/user-attachments/assets/e995c17e-d1e4-4903-8dd8-61df5f025ae3" />
<img width="1889" height="867" alt="Screenshot (3289)" src="https://github.com/user-attachments/assets/f10f901f-137f-480d-bc97-168efb87338a" />


Trang input là nơi người dùng nhập dữ liệu chi phí, baseline business, historical price-demand data, market uncertainty ranges và số lần Monte Carlo simulation. Em đóng góp vào cách tổ chức form thành các nhóm thông tin để người dùng nhập dữ liệu theo trình tự dễ hiểu hơn.

### 3. Loading Screen


<img width="1920" height="859" alt="loading" src="https://github.com/user-attachments/assets/5bac4f01-baba-4a3a-9eeb-b8448e118e3a" />


Loading screen được dùng khi hệ thống đang chạy simulation. Phần này có progress bar, status text, estimated time remaining và phần “Did you know?”. Em thêm và chỉnh phần này để luồng demo mượt hơn, thay vì người dùng bấm chạy mô phỏng rồi chuyển trang quá đột ngột.

### 4. Result Dashboard / Output Screen


<img width="1631" height="754" alt="result1" src="https://github.com/user-attachments/assets/839b04c8-a65b-4f72-ad3b-b5e5948fe03c" />
<img width="1656" height="841" alt="result2" src="https://github.com/user-attachments/assets/fc37cdfb-377f-4f05-a880-274474cbc3e2" />
<img width="1181" height="763" alt="result4" src="https://github.com/user-attachments/assets/38e4f909-4485-4988-96a7-b311763c0722" />
<img width="1595" height="812" alt="result3" src="https://github.com/user-attachments/assets/d1680add-6f1c-4703-84cd-127e77739225" />


Trang output là phần quan trọng nhất trong đóng góp của em. Đây là nơi hiển thị recommendation, KPI cards, biểu đồ, scenario cards và phần phân tích chi tiết. Phần này giúp biến kết quả mô phỏng thành một dashboard trực quan để người dùng có thể hiểu và ra quyết định.

### Phần của em nằm ở đâu trong workflow

<img width="1698" height="926" alt="workflow" src="https://github.com/user-attachments/assets/28f88471-99ef-4b28-a2d2-0166bdd53042" />

Như trong hình workflow ở đây, phần của em là cầu nối giữa cái phần trước và khách hàng. 


## Phần đóng góp đó kết nối thế nào với sản phẩm cuối cùng

Phần em làm là lớp hiển thị cuối cùng của toàn bộ sản phẩm. Các module trước như M1, M2, M3 và M4 tạo ra công thức, dữ liệu, kết quả mô phỏng và logic khuyến nghị. Tuy nhiên, nếu không có M5, người dùng sẽ khó hiểu các kết quả đó và sản phẩm cũng khó demo. Việc có một web rõ ràng giúp người dùng nhập dữ liệu dễ dàng hơn. Các input về chi phí, demand, giá lịch sử và điều kiện thị trường được sắp xếp thành từng nhóm, nên người dùng có thể điền theo một luồng rõ ràng.

Phần này cũng giúp kết quả mô phỏng được trình bày trực quan thay vì chỉ là bảng số. Recommendation được hiển thị rõ ở đầu trang để người dùng biết ngay hệ thống đang đề xuất mức tăng giá nào hay khuyến nghị như thế nào. Sau đó, KPI cards, biểu đồ giúp người dùng hiểu thêm về lợi nhuận tiềm năng, rủi ro và tác động đến nhu cầu và đặc biệt là phần Monte Carlo simulation giúp người dùng thấy được các kịch bản có thể xảy ra nếu họ tăng giá sản phẩm, xác suất lỗ/lời là bao nhiêu và từ đó có cái nhìn tổng thể hơn và ra quyết định.

Cuối cùng là  **3 recommendation: Aggressive, Balanced và Conservative** và **Personalized Insight** là khuyến nghị cuối cùng một cách chi tiết hơn đối với từng mục tiêu khác nhau của khách hàng, và phần insight sau cùng là những phân tích kĩ hơn về số liệu, thị trường,... giúp người dùng có thể nhìn chi tiết những vấn đề gặp phải. 

Qua đó web đã hoàn chỉnh và sẽ hoạt động theo flow như sau: nhập dữ liệu → chạy mô phỏng → xem dashboard → giải thích recommendation.

Nói cách khác, phần đóng góp của em là cầu nối giữa kết quả mô hình và trải nghiệm của người dùng cuối.


## Điều cá nhân học được

Em học được thêm khá nhiều kiến thức về lập trình web, gần như bắt đầu từ con số 0. Trước khi làm dự án, em chưa hiểu rõ một trang web được tạo ra và hoạt động như thế nào. Sau quá trình làm PricePilot, em hiểu hơn vai trò của HTML, CSS, JavaScript và Python trong một web app. Cụ thể, em học được HTML dùng để tạo cấu trúc trang web, CSS dùng để thiết kế giao diện, màu sắc, bố cục và hiệu ứng,... Bên cạnh đó, em cũng hiểu thêm về cách chuyển đổi các dữ liệu tính toán để trình bày cho khách hàng xem

Em học được cách trình bày một dashboard sao cho người dùng dễ hiểu. Một trang kết quả không nên chỉ đưa ra thật nhiều số liệu, mà cần biết chọn chỉ số quan trọng, đặt chúng ở đúng vị trí và giải thích theo logic ra quyết định. Ví dụ, recommendation cần được đặt ở đầu trang, các KPI cần được tách thành từng card, còn biểu đồ và insight cần hỗ trợ người dùng hiểu vì sao hệ thống đưa ra kết quả đó. Qua dự án này, em nhận ra rằng làm web không chỉ là làm cho giao diện đẹp, mà còn là làm cho thông tin trở nên rõ ràng, dễ đọc và có ích cho người dùng cuối.

Một điều quan trọng nữa là em học được rằng cách diễn đạt trong giao diện ảnh hưởng rất nhiều đến cách người dùng hiểu sản phẩm. Khi profit improvement âm, nếu vẫn gọi đó là profit opportunity thì sẽ sai về mặt ý nghĩa. Vì vậy, em phải chỉnh lại wording thành defensive adjustment để dashboard phản ánh đúng logic của mô hình.


## Khó khăn đã gặp và cách xử lý

Khó khăn đầu tiên của em là bắt đầu làm phần web khi gần như chưa có nền tảng về HTML, CSS, JavaScript và Flask. Ban đầu em chưa hiểu rõ một trang web được chia thành cấu trúc, giao diện, tương tác và dữ liệu phía sau như thế nào. Để xử lý, em phải học từng phần nhỏ: HTML để tạo cấu trúc trang, CSS để chỉnh bố cục và giao diện, JavaScript để làm các tương tác như mở modal hoặc ẩn/hiện insight, còn Flask để hiểu cách dữ liệu từ Python được truyền sang trang web. Việc học hỏi về những kiến thức này em đã cần sự hỗ trợ từ các cộng cụ AI, từ đó nắm được cách thức thực hiện

Khó khăn tiếp theo là dữ liệu của kết quả mô phỏng khá nhiều, đặc biệt khi chạy Monte Carlo với nhiều mức price increase và nhiều lần simulation. Nếu đưa quá nhiều dữ liệu lên web cùng lúc hoặc render quá nhiều biểu đồ, dashboard có thể bị chậm hoặc bị lag khi demo. Để xử lý, em không hiển thị toàn bộ dữ liệu mô phỏng thô trên màn hình chính, mà chỉ đưa các chỉ số tổng hợp quan trọng như expected profit, probability of lower profit, average demand và demand loss lên dashboard. Các dữ liệu chi tiết hơn được đưa vào modal riêng để người dùng mở khi cần xem.

Một khó khăn khác là nhiều người dùng có thể không hiểu rõ Monte Carlo là gì, nên nếu trình bày không cẩn thận thì phần này sẽ rất khó hiểu. Để xử lý, em thiết kế phần Monte Carlo Profit Distribution theo hướng trực quan hơn: người dùng có thể chọn từng mức price increase trong dropdown, sau đó xem đồ thị phân phối lợi nhuận tương ứng. Trong modal, em đặt rõ các chỉ số như expected profit, lower profit probability và average demand để người dùng hiểu mỗi biểu đồ đang nói gì. Khi di chuột vào biểu đồ, tooltip cũng hiển thị thông tin cụ thể hơn, giúp người dùng đọc kết quả mà không cần nhìn quá nhiều số liệu cùng lúc.

Ngoài ra khi test lại web với một trường hợp cực xấu và không khả quan, em có lỗi trình bày làm cho web vẫn recommend tăng giá sản phẩm trong khi điều này không mang lại lợi nhuận cho khách hàng tốt hơn so với trường hợp mặc định. Để xử lý vấn đề này, em trình bày lại defensive recommendation, giúp web trình bày lại với khách hàng về trường hợp tối ưu và chỉnh sửa từ profit improvement sang thành profit gap để thấy rõ được chênh lệch về lợi nhuận tiềm năng, giúp khách hàng cân nhắc kĩ hơn.

## Lời nhắn cho sinh viên khóa sau

Nếu sinh viên khóa sau muốn tiếp tục hoặc học từ phần việc này, em nghĩ cần có một chút nền tảng về code, sau đó cần đặt mình vào khách hàng, hiểu rõ trình bày như thế nào thì hợp lý và thuận mắt nhất, dễ tiếp cận với nội dung muốn truyền tải.

Các bạn nên test sản phẩm với nhiều bộ input khác nhau, đặc biệt là các trường hợp xấu như profit improvement âm, downside risk cao hoặc demand loss lớn. Nếu chỉ test với dữ liệu đẹp, dashboard có thể trông ổn nhưng khi gặp tình huống thực tế hơn thì wording và logic hiển thị rất dễ bị sai. ví dụ điển hình như case ở trên. 

Nếu tiếp tục phát triển PricePilot, em nghĩ nên thêm database để lưu lịch sử mô phỏng, thêm user account, và kết nối dữ liệu thị trường thật như giá nguyên vật liệu hoặc chỉ số ngành. Và cần có cách hay hơn để tính toán elasticity. Phần dashboard cũng có thể phát triển thêm chức năng export report để người dùng tải kết quả thành PDF.



**Individual footprint**

**Đỗ Thị Quỳnh Anh \- 2313380004**

1. **Vai trò trong dự án**

Trong dự án PricePilot, em đóng vai trò là M1, phụ trách phần **Economic Logic & Pricing Model**. Phần việc của em là xây dựng logic kinh tế phía sau app, tức là xác định khi doanh nghiệp thay đổi giá bán thì nhu cầu, chi phí và lợi nhuận sẽ thay đổi như thế nào.

Bên cạnh đó, em tập trung vào việc xây dựng các công thức chính của mô hình, đặc biệt là price elasticity, dự báo nhu cầu mới, tính giá bán cơ sở và tính lợi nhuận cho từng kịch bản giá. Đây là phần nền tảng để các thành viên khác có thể tiếp tục phát triển phần mô phỏng, recommendation và giao diện kết quả.

2. **Dấu ấn cá nhân trong sản phẩm**

Đóng góp rõ ràng nhất của em là phần mô hình định giá (pricing model) và các công thức kinh tế được sử dụng trong hệ thống. Toàn bộ quá trình mô phỏng của PricePilot đều dựa trên các công thức mà em thiết kế, đặc biệt là:

* Công thức tính Price Elasticity từ dữ liệu lịch sử.  
* Công thức dự báo nhu cầu mới sau khi thay đổi giá.  
* Công thức tính giá bán đề xuất dựa trên chi phí và tỷ suất lợi nhuận mục tiêu.  
* Công thức tính doanh thu và lợi nhuận cho từng kịch bản giá.

Những công thức này là nền tảng để Monte Carlo Simulation có thể hoạt động và đưa ra khuyến nghị tăng giá phù hợp.

3. **Những việc đã thực sự làm**

### **Việc 1: Tìm hiểu bài toán pricing của doanh nghiệp cơ khí SME**

Em tìm hiểu bối cảnh ra quyết định giá của doanh nghiệp sản xuất cơ khí vừa và nhỏ. Em xác định rằng khi doanh nghiệp muốn tăng giá, họ không thể chỉ nhìn vào chi phí tăng lên, mà còn phải cân nhắc xem khách hàng có tiếp tục đặt hàng hay không. Vì vậy, em tập trung vào mối quan hệ giữa giá bán, nhu cầu, chi phí và lợi nhuận.

### **Việc 2: Thiết kế công thức dự báo demand sau khi tăng giá**

Em xây dựng logic để app dự báo nhu cầu mới khi doanh nghiệp thử các mức tăng giá khác nhau. Trong công thức này, demand không chỉ bị ảnh hưởng bởi price increase, mà còn chịu tác động của các yếu tố thị trường như market growth, customer budget pressure và material shock.

Công thức chính là:

New Demand \= Base Demand × (1 \+ Market Growth − Budget Pressure − Material Shock − Elasticity × Price Increase)

Phần này giúp hệ thống phản ánh được việc giá tăng có thể làm demand giảm, thay vì giả định demand luôn giữ nguyên.

### **Việc 3: Xây dựng cost structure model**

Em tham gia xây dựng logic tính chi phí sản xuất của doanh nghiệp, gồm chi phí nguyên vật liệu, waste rate, nhân công, điện và thuê mặt bằng, bảo trì và khấu hao máy móc. Những chi phí này được dùng để tính tổng chi phí hàng tháng và cost per order.

Cụ thể, em xác định các nhóm chi phí chính:

* Material cost.  
* Waste-adjusted material cost.  
* Labor cost.  
* Electricity and rent.  
* Maintenance cost.  
* Depreciation.  
* Fixed cost.  
* Variable cost per order.  
* Fixed cost per order.

### **Việc 4: Xây dựng công thức base price và current profit**

Sau khi có cost per order, em xây dựng công thức tính base price dựa trên target margin mà doanh nghiệp mong muốn. Từ đó, hệ thống có thể tính được current expected profit làm baseline để so sánh với các kịch bản tăng giá.

Các công thức chính gồm:

Base Price \= Cost per Order / (1 − Target Margin)

Current Profit \= (Base Price − Cost per Order) × Base Demand

### **Việc 5: Kết nối demand forecast với profit calculation**

Em xây dựng logic để sau khi hệ thống tính được demand mới, app sẽ tiếp tục tính selling price mới, cost per order mới và expected profit cho từng mức tăng giá. Phần này giúp app đánh giá được một mức tăng giá có thật sự tốt hay không.

Logic chính là:

* Giá tăng → selling price mới cao hơn.  
* Nhưng giá tăng cũng có thể làm demand giảm.  
* Demand giảm làm số đơn hàng ít hơn.  
* Khi demand thay đổi, fixed cost per order cũng thay đổi.  
* Cuối cùng, app tính profit để xem kịch bản đó có tốt hơn baseline hay không.

### **Việc 6: Kiểm tra tính hợp lý của công thức demand**

Trong quá trình làm, em kiểm tra kết quả mô phỏng để xem demand có phản ứng hợp lý khi price increase thay đổi hay không. Ban đầu công thức demand chưa phản ánh đủ tác động của elasticity, dẫn đến trường hợp giá tăng cao nhưng demand gần như không thay đổi. Sau khi phát hiện vấn đề này, em rà soát lại công thức và điều chỉnh để price increase tác động trực tiếp đến demand thông qua elasticity.

### **Việc 7: Hỗ trợ phân loại và giải thích kết quả kinh tế**

Em hỗ trợ xây dựng cách diễn giải các kết quả như profit improvement, demand loss, risk level và elasticity level. Thay vì chỉ hiển thị con số, hệ thống phân loại kết quả thành các mức như low, moderate, high, meaningful hoặc strong để người dùng dễ hiểu hơn.

Phần này giúp dashboard không chỉ có kết quả tính toán, mà còn có ý nghĩa quản trị rõ ràng hơn.

**4\. File, tính năng, dữ liệu, logic, giao diện, tài liệu hoặc phần demo đã đóng góp**

### **Logic và tính năng đã đóng góp**

* Xây dựng công thức tính Price Elasticity từ dữ liệu lịch sử.  
* Xây dựng Demand Forecasting Logic để dự báo nhu cầu sau khi thay đổi giá bán.  
* Xây dựng Cost Structure Model dùng để tính cost per order.  
* Xây dựng công thức Base Price dựa trên chi phí và target margin.  
* Xây dựng Profit Calculation Model để tính lợi nhuận cho từng kịch bản giá.  
* Tham gia kiểm tra và điều chỉnh logic khi kết quả mô phỏng chưa phản ánh đúng thực tế kinh doanh.

### **Phần thể hiện trong sản phẩm cuối cùng**

Các đóng góp của em được thể hiện trong:

* Historical Data for Fixed Elasticity.  
* Business Baseline Inputs.  
* Demand vs Price Increase Chart.  
* Profit vs Price Increase Chart.  
* Scenario Comparison.  
* Recommendation Engine (Aggressive, Balanced, Conservative).  
* Personalized Insight.  
* Market Condition Analysis.

**5\. Bằng chứng đóng góp**

Link công thức: [**https://docs.google.com/spreadsheets/d/1YP506e8sjTiZqmOY9fNb6fcVjwMv5qI\_kQSa1qlXRuQ/edit?usp=sharing**](https://docs.google.com/spreadsheets/d/1YP506e8sjTiZqmOY9fNb6fcVjwMv5qI_kQSa1qlXRuQ/edit?usp=sharing)

Link task allocation: [**https://docs.google.com/spreadsheets/d/1p9vzLOrRWNIL22DaK8M-8HWok-ZvLx\_OltRTsL\_GEoc/edit?usp=sharing**](https://docs.google.com/spreadsheets/d/1p9vzLOrRWNIL22DaK8M-8HWok-ZvLx_OltRTsL_GEoc/edit?usp=sharing)

Trong code, đóng góp của em có thể kiểm tra ở các hàm classify\_profit\_improvement(value), classify\_demand\_loss(value), classify\_risk(value), classify\_elasticity(value), classify\_fixed\_cost\_share(value), build\_strategy\_text(...), build\_personalized\_insight(...), và phần chọn strategy trong compute\_result\_context(form). Các phần này thể hiện việc em không chỉ xây dựng công thức tính toán, mà còn tham gia thiết kế cách hệ thống diễn giải kết quả pricing thành các mức profit, demand loss, risk và recommendation để người dùng dễ ra quyết định.

1. **Phần đóng góp đó kết nối thế nào với sản phẩm cuối cùng**

Phần việc của em là nền tảng để app có thể tính toán và đưa ra kết quả. Khi người dùng nhập dữ liệu về chi phí, nhu cầu, giá bán cũ, giá bán mới và các yếu tố thị trường, hệ thống sẽ dùng logic kinh tế em xây dựng để chuyển các dữ liệu đó thành các kết quả cụ thể.

Ví dụ, từ dữ liệu lịch sử, app tính được elasticity. Sau đó, khi thử các mức tăng giá khác nhau, app dùng elasticity để ước tính demand mới. Từ demand mới và selling price mới, hệ thống tiếp tục tính cost per order và expected profit.

Những kết quả này sau đó được dùng trong Monte Carlo Simulation và recommendation engine để đề xuất các chiến lược tăng giá như Conservative, Balanced hoặc Aggressive. Vì vậy, phần em làm giúp app có cơ sở kinh tế để đưa ra khuyến nghị, thay vì chỉ tính toán một cách ngẫu nhiên.

2. **Điều cá nhân học được**

Qua phần việc này, em học được cách biến kiến thức kinh tế thành một mô hình có thể áp dụng trong sản phẩm thực tế. Trước đây, em chỉ hiểu price elasticity hay profit analysis dưới dạng lý thuyết, nhưng khi làm dự án này, em phải suy nghĩ xem công thức đó sẽ được đưa vào app như thế nào và kết quả có dễ hiểu với người dùng hay không.

Em cũng học được rằng một mô hình tốt không nhất thiết phải quá phức tạp. Điều quan trọng là mô hình phải rõ ràng, hợp lý và giải thích được. Ngoài ra, em hiểu hơn về cách phối hợp với các thành viên khác, vì phần logic kinh tế của em cần kết nối với phần data input, simulation, recommendation và giao diện kết quả.

3. **Khó khăn đã gặp và cách xử lý**

Khó khăn lớn nhất của em là xây dựng công thức dự báo nhu cầu (demand forecast) sao cho kết quả phản ánh đúng thực tế kinh doanh.

Ban đầu, em đã xây dựng công thức tính demand dựa trên industry growth, income growth và elasticity. Tuy nhiên, sau khi chạy thử mô hình, em nhận thấy kết quả chưa hợp lý. Trong một số trường hợp, dù giá bán tăng khá nhiều (ví dụ 20%) nhưng demand gần như không thay đổi hoặc giảm rất ít. Điều này không phù hợp với logic kinh tế vì trên thực tế khách hàng thường sẽ phản ứng khi giá tăng mạnh.

Để xử lý vấn đề này, em đã rà soát lại công thức và kiểm tra mối quan hệ giữa elasticity và mức tăng giá. Sau khi trao đổi với các thành viên trong nhóm và thử nghiệm với nhiều bộ dữ liệu khác nhau, em điều chỉnh lại công thức để tác động của price increase được phản ánh trực tiếp vào demand thông qua elasticity. Đồng thời, em sửa lại các yếu tố thị trường như market growth, customer budget pressure và material shock để mô hình phản ánh thực tế tốt hơn.

Sau khi điều chỉnh, kết quả mô phỏng trở nên hợp lý hơn. Khi giá tăng cao, demand giảm theo mức độ phù hợp với elasticity, từ đó các kết quả về doanh thu, lợi nhuận và recommendation cũng đáng tin cậy hơn.

4. **Lời nhắn cho sinh viên khóa sau**

Nếu sinh viên khóa sau muốn tiếp tục phần việc này, em nghĩ điều quan trọng nhất là không nên bắt đầu từ code ngay, mà nên hiểu thật rõ bài toán pricing trước. Cần hiểu rằng tăng giá không đồng nghĩa với lợi nhuận chắc chắn tăng, vì khi giá tăng thì khách hàng có thể đặt hàng ít hơn. Vì vậy, phần quan trọng nhất của mô hình là phải giải thích được mối quan hệ giữa price, demand, cost và profit.

Khi xây dựng công thức, nên kiểm tra kết quả bằng những ví dụ đơn giản trước. Nếu giá tăng nhưng demand gần như không đổi, thì mô hình có thể đang chưa phản ánh đúng tác động của elasticity. Ngược lại, nếu demand giảm quá mạnh ở mức tăng giá nhỏ, công thức cũng cần được xem lại. Việc test bằng các tình huống cực đoan sẽ giúp phát hiện lỗi logic sớm hơn.

Ngoài ra, nếu muốn phát triển PricePilot tốt hơn, khóa sau có thể cải thiện phần elasticity bằng cách dùng nhiều điểm dữ liệu lịch sử hơn, hoặc tính elasticity riêng cho từng nhóm khách hàng/từng loại sản phẩm. Như vậy recommendation sẽ sát thực tế hơn thay vì dùng một mức elasticity cố định cho toàn bộ mô phỏng.

Cuối cùng, em nghĩ phần logic kinh tế cần được viết rõ ràng và dễ giải thích. Một mô hình không chỉ cần chạy được, mà còn phải giúp người dùng hiểu vì sao app đưa ra kết quả đó. Khi đi demo hoặc bảo vệ, nếu mình giải thích được công thức và lý do chọn công thức, sản phẩm sẽ thuyết phục hơn rất nhiều.


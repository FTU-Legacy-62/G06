# Group Footprint

## Tên sản phẩm

**PricePilot**

## Mã nhóm

**G06**

## Link repo

https://github.com/FTU-Legacy-62/G06

## Link demo

https://pricepiloot.onrender.com/


## Vấn đề nhóm muốn giải quyết

Nhóm muốn giải quyết vấn đề ra quyết định tăng giá trong các doanh nghiệp sản xuất cơ khí vừa và nhỏ. Trong thực tế, các doanh nghiệp này thường phải đối mặt với nhiều áp lực cùng lúc như giá nguyên vật liệu tăng, chi phí nhân công, chi phí cố định, biến động nhu cầu thị trường và mức độ nhạy cảm của khách hàng với thay đổi giá.

Vấn đề xảy ra trong bối cảnh doanh nghiệp cần điều chỉnh giá bán để bảo vệ lợi nhuận, nhưng nếu tăng giá quá cao thì có thể mất đơn hàng. Ngược lại, nếu giữ giá quá thấp thì doanh nghiệp có thể không bù được chi phí sản xuất và rủi ro thị trường.

Đối tượng bị ảnh hưởng trực tiếp là chủ doanh nghiệp, quản lý sản xuất, bộ phận tài chính, bộ phận bán hàng và những người tham gia quyết định báo giá trong doanh nghiệp cơ khí. Những người này cần một công cụ hỗ trợ để xem nhiều kịch bản giá khác nhau, thay vì chỉ ra quyết định dựa trên cảm tính.


## Người dùng mục tiêu

Người dùng chính của PricePilot là các doanh nghiệp gia công cơ khí vừa và nhỏ 

Họ cần một công cụ giúp trả lời các câu hỏi như:

* Có nên tăng giá bán hay không?
* Nếu tăng giá thì nên tăng khoảng bao nhiêu %?
* Việc tăng giá có thể làm lợi nhuận thay đổi như thế nào?
* Nhu cầu có thể giảm bao nhiêu nếu giá tăng?
* Rủi ro lợi nhuận thấp hơn hiện tại là bao nhiêu?
* Trong các chiến lược Aggressive, Balanced và Conservative, phương án nào phù hợp hơn?

Người dùng sẽ dùng sản phẩm khi cần đánh giá quyết định điều chỉnh giá bán, lập phương án báo giá, kiểm tra tác động của chi phí nguyên vật liệu hoặc chuẩn bị thảo luận nội bộ về chiến lược giá.


## Sản phẩm hiện làm được gì

PricePilot hiện là một web app mô phỏng quyết định tăng giá dựa trên dữ liệu đầu vào của doanh nghiệp. Sản phẩm cho phép người dùng nhập các thông tin về chi phí, nhu cầu hiện tại, dữ liệu giá và nhu cầu trong quá khứ, cùng các giả định về điều kiện thị trường.

Sau khi người dùng chạy mô phỏng, hệ thống sẽ tạo ra một dashboard kết quả gồm:

* Mức tăng giá được khuyến nghị.
* Lợi nhuận kỳ vọng.
* Mức thay đổi lợi nhuận so với hiện tại.
* Xác suất lợi nhuận thấp hơn mức hiện tại.
* Mức mất nhu cầu trung bình.
* So sánh ba chiến lược định giá: Aggressive, Balanced và Conservative.
* Biểu đồ Profit vs Price Increase.
* Biểu đồ Demand vs Price Increase.
* Modal xem phân phối lợi nhuận Monte Carlo theo từng mức tăng giá.
* Personalized Detailed Insight để giải thích vì sao hệ thống đưa ra khuyến nghị đó.
* Market Condition Analysis để phân tích tác động của market growth, customer budget pressure, material shock impact và material inflation.

Sản phẩm không chỉ hiển thị số liệu đơn lẻ, mà tổ chức kết quả thành một giao diện hỗ trợ ra quyết định. Người dùng có thể nhìn thấy cả lợi nhuận, rủi ro và tác động lên nhu cầu trước khi quyết định có nên tăng giá hay không.


## Input

Sản phẩm nhận các nhóm thông tin đầu vào sau:

### 1. Monthly Cost Inputs

Người dùng nhập các thông tin liên quan đến chi phí sản xuất hàng tháng, gồm:

* Loại nguyên vật liệu: thép, inox, nhôm hoặc đồng.
* Số tấn nguyên vật liệu sử dụng mỗi tháng.
* Tỷ lệ hao hụt nguyên vật liệu.
* Số lượng lao động.
* Lương trung bình mỗi lao động.
* Chi phí điện và thuê mặt bằng mỗi năm.
* Chi phí bảo trì mỗi năm.
* Giá trị máy móc.
* Tuổi thọ máy móc.

### 2. Business Baseline Inputs

Người dùng nhập các thông tin nền của doanh nghiệp:

* Nhu cầu hiện tại hoặc số đơn hàng hiện tại mỗi tháng.
* Target margin mong muốn.

Trong sản phẩm, demand được hiểu là số lượng đơn hàng hoặc job/batch/contract trung bình mỗi tháng, không nhất thiết là số lượng sản phẩm đơn vị.

### 3. Historical Data for Fixed Elasticity

Người dùng nhập dữ liệu lịch sử để hệ thống tính độ co giãn cầu theo giá:

* Giá bán cũ.
* Giá bán mới trong quá khứ.
* Nhu cầu cũ.
* Nhu cầu mới sau khi giá thay đổi.

Dữ liệu này giúp hệ thống ước lượng mức độ khách hàng phản ứng với thay đổi giá.

### 4. Market Uncertainty Ranges

Người dùng chọn các khoảng giả định thị trường để Monte Carlo simulation lấy mẫu:

* Market growth.
* Customer budget pressure.
* Material shock impact.
* Material inflation.
* Mức tăng giá tối đa muốn kiểm tra.

### 5. Monte Carlo Settings

Người dùng chọn số lần mô phỏng cho mỗi mức tăng giá, ví dụ:

* 1,000 simulations.
* 2,000 simulations.
* 3,000 simulations.
* 5,000 simulations.
* 10,000 simulations.
* 20,000 simulations.


## Logic hoặc quy tắc xử lý

PricePilot xử lý input qua các bước chính sau:

### 1. Tính chi phí sản xuất

Hệ thống tính chi phí nguyên vật liệu hàng tháng dựa trên loại vật liệu và số tấn sử dụng. Sau đó chi phí nguyên vật liệu được điều chỉnh theo tỷ lệ hao hụt.

Công thức tổng quát:

```text
Monthly material cost = material price × tons per month
Adjusted material cost = monthly material cost × (1 + waste rate)
Labor cost = number of workers × salary per worker
Fixed cost = electricity and rent / 12 + maintenance / 12 + depreciation
```

Từ đó hệ thống tính:

```text
Variable cost per order = adjusted material cost + labor cost / base demand
Fixed cost per order = fixed cost / base demand
Current cost per order = variable cost per order + fixed cost per order
```

### 2. Tính giá nền hiện tại

Giá nền được tính dựa trên chi phí mỗi đơn hàng và target margin:

```text
Base price = current cost per order / (1 - target margin)
```

Lợi nhuận hiện tại được tính:

```text
Current profit = (base price - current cost per order) × base demand
```

### 3. Tính fixed elasticity từ dữ liệu lịch sử

Hệ thống tính elasticity từ thay đổi giá và thay đổi nhu cầu trong quá khứ:

```text
Elasticity = |% change in demand| / |% change in price|
```

Elasticity được giới hạn trong khoảng hợp lý từ 0.1 đến 3.0 để tránh kết quả quá cực đoan.

Elasticity càng cao thì khách hàng càng nhạy cảm với thay đổi giá. Khi đó, tăng giá có thể khiến nhu cầu giảm mạnh hơn.

### 4. Chạy Monte Carlo simulation

Price increase là biến quyết định của doanh nghiệp. Hệ thống kiểm tra nhiều mức tăng giá từ 0% đến mức tối đa mà người dùng chọn, với bước tăng 0.5%.

Ở mỗi mức tăng giá, Monte Carlo simulation sẽ lấy mẫu ngẫu nhiên các yếu tố thị trường trong khoảng người dùng nhập:

* Market growth.
* Customer budget pressure.
* Material shock impact.
* Material inflation.

Demand change được mô phỏng theo logic:

```text
Demand change = market growth - customer budget pressure - material shock impact - elasticity × price increase
```

Sau đó hệ thống tính:

```text
New demand = base demand × (1 + demand change)
New selling price = base price × (1 + price increase)
New variable cost per order = variable cost per order × (1 + material inflation)
New fixed cost per order = fixed cost / new demand
New profit = (new selling price - new cost per order) × new demand
```

Điểm quan trọng là material inflation ảnh hưởng đến chi phí, còn market growth, customer budget pressure và material shock impact ảnh hưởng đến nhu cầu.

### 5. Tính rủi ro

Với mỗi mức tăng giá, hệ thống so sánh lợi nhuận mô phỏng với lợi nhuận hiện tại để tính xác suất lợi nhuận thấp hơn hiện tại:

```text
Probability of lower profit = số lần profit mô phỏng < current profit / tổng số lần mô phỏng
```

Chỉ số này giúp người dùng thấy downside risk, không chỉ thấy lợi nhuận kỳ vọng.

### 6. Tạo ba chiến lược

Hệ thống chia kết quả thành ba chiến lược:

**Aggressive:**
Chiến lược ưu tiên lợi nhuận kỳ vọng cao nhất trong các khoảng giá được kiểm tra. Phương án này có thể tạo upside cao hơn, nhưng thường đi kèm demand loss và downside risk lớn hơn.

**Balanced:**
Chiến lược chính của sản phẩm. Balanced cố gắng chọn mức tăng giá có lợi nhuận kỳ vọng tốt, đồng thời vẫn kiểm soát demand loss và probability of lower profit. Đây là phương án được dùng làm top recommendation.

**Conservative:**
Chiến lược ưu tiên giữ nhu cầu ổn định và giảm rủi ro. Conservative phù hợp khi doanh nghiệp lo ngại mất đơn hàng hoặc khách hàng nhạy cảm với giá.

### 7. Defensive recommendation

Nếu profit improvement của recommendation nhỏ hơn 0, hệ thống không trình bày kết quả như một cơ hội tăng lợi nhuận. Thay vào đó, dashboard hiển thị theo hướng defensive recommendation.

Trong trường hợp này, hệ thống sẽ giải thích rằng không có kịch bản nào thật sự tạo lợi nhuận cao hơn baseline hiện tại dưới các giả định đang nhập. Recommendation khi đó được hiểu là phương án phòng thủ tốt hơn trong các kịch bản xấu, chứ không phải tín hiệu chắc chắn nên tăng giá để tăng lợi nhuận.


## User flow

User flow chính của PricePilot gồm các bước:

1. Người dùng mở trang giới thiệu PricePilot.
2. Người dùng đọc mô tả ngắn hoặc mở phần Detail để hiểu sản phẩm hoạt động như thế nào.
3. Người dùng bấm Start để vào trang nhập liệu.
4. Người dùng nhập dữ liệu chi phí, dữ liệu doanh nghiệp, dữ liệu lịch sử về giá và demand.
5. Người dùng chọn các khoảng giả định thị trường và số lần Monte Carlo simulation.
6. Người dùng bấm Run Simulation.
7. Sản phẩm hiển thị trang loading trong khi backend chạy mô phỏng.
8. Sau khi mô phỏng hoàn thành, sản phẩm chuyển sang trang Result Dashboard.
9. Người dùng xem top recommendation, KPI, biểu đồ profit, biểu đồ demand và ba scenario.
10. Người dùng mở Personalized Detailed Insight để xem giải thích chi tiết.
11. Người dùng có thể mở modal Monte Carlo Profit Distribution để xem phân phối lợi nhuận theo từng mức tăng giá.
12. Người dùng có thể quay lại input page để thay đổi giả định và chạy lại simulation.


## Output

Sản phẩm tạo ra các output chính sau:

### 1. Top recommendation

Dashboard hiển thị mức tăng giá được khuyến nghị. Nếu profit improvement không âm, hệ thống hiển thị:

```text
Top Recommendation
Increase price by X%
```

Nếu profit improvement âm, hệ thống hiển thị:

```text
Defensive Recommendation
Increase price by X%
No fully profitable scenario found under current assumptions.
```

### 2. Các chỉ số chính

Các chỉ số chính bao gồm:

* Current base price.
* Current expected profit.
* Recommended price increase range 
* Expected profit.
* Best single price increase.
* Profit improvement hoặc profit gap so với current profit.
* Probability of lower profit.
* Average demand.
* Average demand loss.
* Number of simulations.

### 3. Biểu đồ

Sản phẩm tạo ra hai biểu đồ chính:

* Profit vs Price Increase.
* Demand vs Price Increase.

Các biểu đồ giúp người dùng nhìn thấy khi giá tăng thì lợi nhuận và nhu cầu thay đổi như thế nào.

### 4. Scenario recommendations

Sản phẩm so sánh ba chiến lược:

* Aggressive.
* Balanced.
* Conservative.

Mỗi scenario có range tăng giá, expected profit, profit improvement hoặc profit gap, risk, demand loss và phần advisory text riêng.

### 5. Monte Carlo Profit Distribution

Người dùng có thể mở tab Monte Carlo Profit Distribution để chọn từng mức tăng giá và xem phân phối lợi nhuận mô phỏng tại mức đó. Biểu đồ này giúp thể hiện độ bất định của kết quả và rủi ro profit thấp hơn baseline.

### 6. Personalized Detailed Insight

Sản phẩm tạo một phần phân tích chi tiết gồm:

* Executive recommendation.
* Decision scorecard.
* Market Condition Analysis.
* Why this recommendation was selected.
* Main pressure driver behind demand change.
* Customer sensitivity and cost structure diagnosis.
* Implementation plan.


## Các lựa chọn thiết kế quan trọng

### 1. Chọn vấn đề để thực hiện bài và chọn đối tượng mục tiêu

Ý tưởng ban đầu của nhóm là xây dựng một web app hỗ trợ doanh nghiệp ra quyết định về giá bán sản phẩm. Tuy nhiên, khi phát triển ý tưởng này, nhóm nhận ra rằng bài toán khuyến nghị giá không thể áp dụng phù hợp cho mọi ngành. Để mô hình có ý nghĩa, ngành được chọn cần có mức độ cạnh tranh đủ cao và không bị chi phối bởi một doanh nghiệp lớn duy nhất. Nếu thị trường bị một doanh nghiệp lớn dominate, quyết định giá sẽ phụ thuộc nhiều vào quyền lực thị trường, thương hiệu hoặc vị thế dẫn đầu, khiến việc mô phỏng phản ứng của demand và rủi ro khi tăng giá trở nên kém phù hợp.

Vì vậy, nhóm chọn các doanh nghiệp vừa và nhỏ trong ngành gia công cơ khí làm đối tượng mục tiêu. Nhóm doanh nghiệp này đáp ứng tốt các điều kiện trên: thị trường có tính cạnh tranh, các doanh nghiệp thường không có quyền lực định giá quá lớn, và quyết định tăng giá có thể ảnh hưởng trực tiếp đến khả năng giữ đơn hàng. Trong bối cảnh đó, một công cụ hỗ trợ mô phỏng tác động của việc tăng giá lên lợi nhuận, nhu cầu và rủi ro sẽ phù hợp hơn với nhu cầu thực tế của người dùng.

### 2. Vì sao chọn price elasticity of demand làm economic logic của bài?

Nhóm chọn price elasticity of demand vì bài toán chính của PricePilot là xem việc tăng giá sẽ ảnh hưởng thế nào đến nhu cầu. Khi doanh nghiệp tăng giá, demand thường sẽ giảm, nhưng giảm nhiều hay ít còn tùy vào mức độ nhạy cảm của khách hàng với giá.

Price elasticity giúp thể hiện đúng ý này. Nếu elasticity cao, khách hàng nhạy cảm với giá hơn, nên chỉ cần tăng giá một chút thì demand có thể giảm mạnh. Nếu elasticity thấp, khách hàng ít nhạy cảm hơn, doanh nghiệp có thể tăng giá mà không mất quá nhiều đơn hàng.

Trong PricePilot, elasticity được tính từ dữ liệu cũ của doanh nghiệp, gồm giá cũ, giá mới, nhu cầu cũ và nhu cầu mới. Nhờ vậy, phần tính demand không chỉ dựa trên cảm tính, mà có một logic kinh tế rõ ràng để ước lượng demand ở các mức tăng giá khác nhau.

### 3. Vì sao chọn Monte Carlo simulation?

Nhóm chọn Monte Carlo simulation vì bài toán định giá trong PricePilot không phải là một bài toán có kết quả chắc chắn. Khi doanh nghiệp quyết định tăng giá, kết quả cuối cùng không chỉ phụ thuộc vào mức giá mới, mà còn phụ thuộc vào nhiều yếu tố thị trường có tính bất định như tăng trưởng nhu cầu, áp lực ngân sách của khách hàng, biến động nguyên vật liệu và lạm phát chi phí.

Nếu chỉ dùng một kịch bản cố định, sản phẩm sẽ chỉ cho ra một kết quả duy nhất, trong khi thực tế có thể xảy ra nhiều tình huống khác nhau. Monte Carlo phù hợp với PricePilot vì người dùng có thể nhập các khoảng giả định, sau đó hệ thống mô phỏng nhiều lần để xem kết quả có thể dao động như thế nào.

Nhờ đó, web không chỉ hiển thị expected profit, mà còn cho thấy average demand, demand loss và probability of lower profit. Điều này giúp người dùng không chỉ biết phương án nào có lợi nhuận kỳ vọng tốt hơn, mà còn hiểu được mức độ rủi ro trước khi ra quyết định.

### 4. Chọn ba chiến lược khuyến nghị khách hàng: Aggressive, Balanced và Conservative

Thay vì chỉ đưa ra một mức tăng giá duy nhất, nhóm chọn trình bày ba chiến lược: Aggressive, Balanced và Conservative. Lý do là trong thực tế, mỗi doanh nghiệp có mức chấp nhận rủi ro khác nhau.

Aggressive phù hợp với doanh nghiệp muốn tối đa hóa lợi nhuận kỳ vọng, Balanced là phương án chính để cân bằng giữa profit, demand loss và risk, còn Conservative phù hợp với doanh nghiệp muốn bảo vệ nhu cầu và giảm rủi ro. Cách chia này giúp sản phẩm giống một công cụ hỗ trợ quyết định hơn là một phép tính một chiều.

### 5. Chọn defensive recommendation khi kết quả không tốt hơn hiện tại

Trong quá trình test sản phẩm, nhóm gặp trường hợp mức tăng giá được khuyến nghị vẫn có profit thấp hơn current baseline. Nếu dashboard vẫn hiển thị như một “profit opportunity” bình thường, người dùng có thể hiểu sai rằng hệ thống đang khuyến nghị tăng giá để chắc chắn tăng lợi nhuận.

Vì vậy, nhóm thêm cách hiển thị Defensive Recommendation. Khi profit improvement âm, hệ thống sẽ giải thích rằng không có kịch bản nào thật sự tốt hơn hiện tại dưới các giả định đang nhập. Trong trường hợp đó, recommendation được hiểu là phương án phòng thủ hoặc phương án ít rủi ro hơn trong bối cảnh bất lợi, chứ không phải một cơ hội tăng lợi nhuận chắc chắn.

Lựa chọn này giúp sản phẩm trung thực hơn với kết quả mô phỏng và làm dashboard dễ giải thích hơn khi demo.

## Điểm nhóm thấy làm tốt

Nhóm thấy sản phẩm làm tốt ở một số điểm sau:

### 1. Giao diện dashboard rõ ràng

Trang result dashboard được thiết kế theo logic ra quyết định: top recommendation, KPI, biểu đồ, scenario comparison và detailed insight. Cách trình bày này giúp người dùng không chỉ xem số liệu mà còn hiểu được ý nghĩa của kết quả.

### 2. Có mô phỏng rủi ro thay vì chỉ tính lợi nhuận trung bình

Sản phẩm không chỉ tính expected profit, mà còn tính probability of lower profit. Đây là điểm quan trọng vì khi đưa ra quyết định về giá bán, một phương án có lợi nhuận kỳ vọng cao nhưng rủi ro quá lớn có thể không phù hợp.

### 3. Có so sánh nhiều chiến lược

Việc chia thành Aggressive, Balanced và Conservative giúp người dùng có nhiều lựa chọn. Sản phẩm của nhóm không ép người dùng chỉ theo một phương án, mà cho họ cơ sở để cân nhắc theo mức độ chấp nhận rủi ro.

### 4. Có Personalized Detailed Insight

Phần insight giúp giải thích vì sao recommendation được chọn, demand loss có ý nghĩa gì, risk level ra sao và yếu tố nào đang tạo áp lực lớn nhất.
### 5. Có Market Condition Analysis

Phần Market Condition Analysis giúp tách riêng phân tích về thị trường. Nó cho biết market growth đang hỗ trợ demand bao nhiêu, customer budget pressure và material shock đang gây áp lực bao nhiêu, net market effect trước price elasticity là gì, và material inflation ảnh hưởng tới chi phí như thế nào.


## Hạn chế hiện tại

Sản phẩm hiện vẫn còn một số hạn chế:

### 1. Dữ liệu đầu vào phụ thuộc vào giả định của người dùng

Các biến như market growth, customer budget pressure, material shock impact và material inflation đều do người dùng nhập dưới dạng khoảng giả định. Nếu người dùng nhập dữ liệu không sát thực tế, kết quả mô phỏng cũng có thể bị lệch.

### 2. Chưa kết nối dữ liệu thị trường thật theo thời gian thực

Sản phẩm chưa tự động lấy dữ liệu về giá nguyên vật liệu, nhu cầu ngành hoặc chỉ số kinh tế từ nguồn bên ngoài. Các dữ liệu thị trường hiện được nhập thủ công.

### 3. Elasticity còn đơn giản

Elasticity được tính từ một cặp dữ liệu giá và nhu cầu trong quá khứ. Trong thực tế, elasticity có thể thay đổi theo nhóm khách hàng, loại sản phẩm, mùa vụ, đối thủ cạnh tranh và chất lượng dịch vụ.

### 4. Chưa có database

Sản phẩm hiện chưa lưu lịch sử mô phỏng dài hạn. Kết quả chủ yếu được xử lý trong session/cache khi người dùng chạy app.

### 5. Chưa có phân quyền người dùng

Sản phẩm chưa có đăng nhập, phân quyền hoặc lưu hồ sơ doanh nghiệp riêng cho từng user.

### 6. Chưa tối ưu hoàn toàn cho quy mô lớn

Sản phẩm đã được tối ưu để chạy trên môi trường demo, nhưng nếu mở rộng cho nhiều người dùng thật cùng lúc thì cần cải thiện backend, lưu trữ và hiệu năng.



## Điều nhóm học được

Qua quá trình làm PricePilot, nhóm học được nhiều điều:

### 1. Hiểu vấn đề người dùng trước khi làm tính năng

Nhóm nhận ra rằng một sản phẩm tốt không chỉ cần có công thức hoặc thuật toán, mà còn phải giải thích được kết quả theo cách người dùng hiểu và ra quyết định được.

### 2. Học cách biến một vấn đề tài chính thành sản phẩm tương tác

Pricing decision ban đầu là một bài toán tính toán, nhưng nhóm đã chuyển nó thành một web app có input, mô phỏng, dashboard và recommendation.

### 3. Học cách xây dựng logic mô phỏng

Nhóm học được cách kết hợp cost structure, elasticity, demand change, material inflation và Monte Carlo simulation để tạo ra kết quả có tính bất định và rủi ro.

### 4. Học cách thiết kế dashboard

Nhóm học cách sắp xếp kết quả theo thứ tự một cách logic: recommendation trước, KPI sau, rồi đến biểu đồ và phần giải thích chi tiết.

### 5. Học cách giải thích model

Nhóm học được rằng nếu sản phẩm chỉ đưa ra con số thì người dùng có thể khó tin hoặc khó hiểu. Vì vậy, phần personalized insight và market analysis rất quan trọng để giải thích logic đằng sau recommendation.

### 6. Học cách triển khai sản phẩm

Nhóm học cách đưa sản phẩm từ file Python local lên GitHub và deploy lên Render. Quá trình này giúp nhóm hiểu thêm về requirements.txt, start command, lỗi deploy và cách kiểm tra logs.

### 7. Học cách làm việc nhóm

Nhóm học cách chia việc giữa ý tưởng, logic, code, giao diện, kiểm thử, tài liệu và chuẩn bị demo. Nhóm cũng học được rằng cần ghi lại quá trình làm việc để footprint phản ánh đúng đóng góp của cả nhóm.



## Gợi ý cho khóa sau

Nếu sinh viên khóa sau muốn tiếp tục hoặc học từ sản phẩm này, nhóm có một số gợi ý:

### 1. Nên bắt đầu từ việc hiểu bài toán pricing

Trước khi code, nên hiểu rõ người dùng là ai, họ ra quyết định giá trong bối cảnh nào và họ cần xem chỉ số gì.

### 2. Nên kiểm tra kỹ dữ liệu đầu vào

Các input như demand, price, cost, elasticity và market assumptions ảnh hưởng rất mạnh đến output. Nếu input không hợp lý, kết quả có thể gây hiểu nhầm.

### 3. Nên mở rộng dữ liệu thị trường

Khóa sau có thể kết nối thêm dữ liệu giá nguyên vật liệu, chỉ số ngành sản xuất, lạm phát hoặc dữ liệu nhu cầu thực tế để mô hình sát thị trường hơn.

### 4. Nên phát triển database và user account

Nếu muốn biến PricePilot thành sản phẩm thật hơn, có thể thêm database để lưu lịch sử mô phỏng, cho phép người dùng so sánh nhiều lần chạy và quản lý nhiều sản phẩm hoặc khách hàng khác nhau.

### 5. Nên cải thiện elasticity model

Có thể tính elasticity theo từng nhóm khách hàng, từng loại sản phẩm hoặc dùng nhiều điểm dữ liệu lịch sử hơn thay vì chỉ một cặp old/new price-demand.

### 6. Nên giữ dashboard đơn giản

Dù model có thể phức tạp, giao diện người dùng nên đơn giản và rõ ràng. Người dùng cần hiểu recommendation, risk và demand impact trước, sau đó mới xem các phân tích sâu hơn.

### 7. Nên test sản phẩm trên môi trường deploy sớm

Không nên đợi gần deadline mới deploy. Một số lỗi chỉ xuất hiện trên Render hoặc môi trường online, ví dụ thiếu package, sai start command, hoặc quá tải khi chạy nhiều simulation.


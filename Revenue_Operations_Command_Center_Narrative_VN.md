# Trung Tâm Điều Hành Hoạt Động Doanh Thu — Tường Thuật Dashboard

> **Tác giả:** Alexander Marvin  
> **Ngày:** Tháng 4, 2026  
> **Công cụ:** Salesforce Lightning (Phiên bản Developer)  
> **Dữ liệu:** 100 Tài khoản, 100 Liên hệ, 100 Cơ hội, 100 Lead (dữ liệu mẫu)  
> **Mục đích:** Thể hiện khả năng điều hành RevOps — cung cấp góc nhìn tổng thể về sức khỏe pipeline, độ tin cậy dự báo, phân bổ chất lượng lead, ROI theo kênh, hiệu suất ngành, và năng suất nhân viên trên toàn bộ hệ thống doanh thu.

---

## Tóm Tắt Điều Hành

Dashboard này là trung tâm thần kinh vận hành cho Hoạt Động Doanh Thu. Nó trả lời các câu hỏi mà lãnh đạo RevOps đặt ra mỗi sáng thứ Hai: Pipeline hiện có bao nhiêu? Mức độ tin cậy ra sao? Giao dịch đang bị trì hoãn ở đâu? Kênh và ngành nào đang tạo ra nhiều giá trị nhất? Và nhân viên nào cần đào tạo so với nhân viên nào nên được nghiên cứu để học hỏi? Khác với góc nhìn tập trung vào chuyển đổi, dashboard này được xây dựng cho quản lý pipeline hàng ngày — làm nổi bật các đòn bẩy mà đội ops có thể sử dụng để cải thiện độ chính xác dự báo, tăng tốc giao dịch, và cân bằng khối lượng công việc trong đội.

---

## 📊 Hướng Dẫn Chi Tiết Dashboard

### HÀNG 1: KPI Điều Hành — Pipeline, Doanh Thu, và Tỷ Lệ Thắng Tổng Quan

#### Doanh Thu Pipeline Đang Mở (Chỉ số)

![Open Pipeline Revenue](screenshots/rocc1_open_pipeline_revenue.png)

| KPI                       |    Giá Trị    |
|---------------------------|---------------|
| Doanh Thu Pipeline Đang Mở| $43,313,544   |

**Điểm Chính:**  
$43.3M trong pipeline đang hoạt động đại diện cho tổng doanh thu mà đội ngũ bán hàng đang theo đuổi. Đây là mẫu số để đo lường tất cả các chỉ số phía sau — tỷ lệ chuyển đổi, độ chính xác dự báo, tốc độ qua từng giai đoạn.

---

#### Giá Trị Giao Dịch Đã Đóng: Thắng vs. Thua (Donut)

![Closed Deal Value Won vs Lost](screenshots/rocc2_closed_deal_value.png)

| Kết Quả      | Giá Trị  | % Đã Đóng  |
|--------------|----------|------------|
| Đóng Thắng   |  $4.7M   |    64%     |
| Đóng Thua    |  $2.7M   |    36%     |
| Tổng Đã Đóng |  $7.4M   |   100%     |

**Điểm Chính:**  
Trong tổng số $7.4M đã rời khỏi pipeline, 64% đã chuyển đổi thành doanh thu ($4.7M) và 36% bị mất ($2.7M). Tỷ lệ thắng theo giá trị là lành mạnh, nhưng $2.7M doanh thu bị mất cần được phân tích nguyên nhân để giảm thiểu tổn thất có thể phòng tránh trong các quý tới.

**Hành Động Đề Xuất:**
- Thực hiện phân tích nguyên nhân thua cho các giao dịch đã đóng-thua để xác định các mẫu hình hoặc phản đối phổ biến.
- Triển khai đào tạo có mục tiêu hoặc cải tiến quy trình để giải quyết các nguyên nhân hàng đầu gây mất doanh thu.
- Xem xét dữ liệu thắng/thua hàng quý để theo dõi tiến độ và tinh chỉnh chiến lược.

---

#### Giao Dịch Đã Đóng: Thắng vs. Thua (Donut)

![Closed Deals Won vs Lost](screenshots/rocc3_closed_deals_count.png)

| Kết Quả      | Số Lượng | % Tổng  |
|--------------|----------|---------|
| Đóng Thắng   |    9     |   60%   |
| Đóng Thua    |    6     |   40%   |
| Tổng Đã Đóng |   15     |  100%   |

**Điểm Chính:**  
Tỷ lệ thắng 60% (9 trên 15 giao dịch đã đóng) là một mức cơ sở vững chắc. Kết hợp với góc nhìn theo giá trị ở trên, đội ngũ đang thắng cả nhiều giao dịch hơn lẫn các giao dịch có giá trị cao hơn — cho thấy việc đánh giá chất lượng giao dịch nhìn chung là hiệu quả. 6 giao dịch thua vẫn cần được xem xét để tìm mẫu hình (giai đoạn thua, ngành, nhân viên, nguồn lead) nhằm ngăn ngừa tổn thất trong tương lai.

**Hành Động Đề Xuất:**  
- Thiết lập lịch xem xét giao dịch thua định kỳ (hàng tuần hoặc hai tuần một lần) để nắm bắt nguyên nhân khi bối cảnh còn mới.
- Đối chiếu các giao dịch thua theo ngành và giai đoạn để xác định xem tổn thất có tập trung ở các phân khúc hoặc giai đoạn pipeline cụ thể hay không.

---

### HÀNG 2: Phễu Pipeline Bán Hàng — Phân Bổ Pipeline Theo Từng Giai Đoạn

![Sales Pipeline Funnel](screenshots/rocc4_sales_pipeline_funnel.png)

| Giai Đoạn           | Giá Trị  | % Tổng ($48M)     |
|---------------------|----------|-------------------|
| Introduction        |  $6.7M   |     ~14%          |
| Discovery           | $13.4M   |    ~27.9%         |
| Specification       |  $6.7M   |     ~14%          |
| Estimate/Quote      |  $9.5M   |    ~19.8%         |
| Finalize/Negotiate  |  $7.1M   |    ~14.8%         |
| Closed Won          |  $4.7M   |    ~9.8%          |
| Total               |  $48M    |    ~100%          |

**Điểm Chính:**
Phễu nặng nhất ở giai đoạn Discovery — $13.4M, chiếm ~27.9% tổng giá trị pipeline. **Sự tập trung này cho thấy các giao dịch đang tích tụ ở giai đoạn Discovery thay vì tiến triển đều đặn.** Discovery thường là giai đoạn tư vấn nhiều nhất trong chu kỳ bán hàng, nơi khách hàng tiềm năng đang xác định yêu cầu và đánh giá sự phù hợp. Khi giao dịch bị trì hoãn ở đây, điều đó thường có nghĩa là khách hàng cần hỗ trợ có cấu trúc hơn — xác định phạm vi rõ ràng hơn, phân tích nhu cầu sâu hơn, hoặc sự liên kết mạnh hơn giữa mục tiêu của họ và giải pháp đề xuất — trước khi có thể tiến sang Specification.

Quan trọng là, phễu **lấp đầy lại sau Specification**: Estimate/Quote giữ $9.5M (19.8%) và Finalize/Negotiate giữ $7.1M (14.8%). Điều này có nghĩa là khi giao dịch vượt qua điểm nghẽn Discovery, chúng có xu hướng tiến triển thuận lợi hơn qua các giai đoạn sau. Ưu tiên vận hành không phải là bịt lỗ rò — mà là tăng tốc dòng chảy qua giai đoạn chuyển tiếp Discovery-sang-Specification.

**Hành Động Đề Xuất:**
- Tập trung nguồn lực hỗ trợ bán hàng vào bước chuyển giao Discovery → Specification. Trang bị cho nhân viên các playbook chuyển đổi, mẫu yêu cầu, và danh sách kiểm tra xác nhận kỹ thuật.
- Xác định các đặc điểm chung của giao dịch di chuyển nhanh qua Discovery — nhân rộng phương pháp đó cho toàn đội.
- Theo dõi chặt chẽ Finalize/Negotiate: $7.1M giao dịch giai đoạn cuối (~14.8% pipeline) đại diện cho doanh thu có thể đóng trong ngắn hạn.

---

### HÀNG 3: Tiếp Nhận & Chất Lượng Lead — Phân Bổ Trạng Thái và Đánh Giá Theo Nguồn

#### Lead Theo Trạng Thái Hiện Tại (Donut)

![Leads by Current Status](screenshots/rocc5_leads_by_status.png)

| Trạng Thái | Số Lượng | % Tổng    |
|------------|-------|------------|
| New        |  35   |    35%     |
| Contacted  |  13   |    13%     |
| Working    |  52   |    52%     |

**Điểm Chính:**
Phần lớn lead (52%) đang ở trạng thái "Working", cho thấy đội ngũ bán hàng đang tích cực tương tác. Chỉ 35% vẫn ở trạng thái "New" (chưa liên hệ và chưa đánh giá), trong khi 13% đã được "Contacted" nhưng chưa tiến triển. Phân bổ này cho thấy hoạt động pipeline mạnh mẽ, nhưng cũng nhấn mạnh tầm quan trọng của việc nhanh chóng đưa lead mới vào trạng thái làm việc tích cực để tối đa hóa cơ hội chuyển đổi.

**Hành Động Đề Xuất:**
- Duy trì trọng tâm vào việc đẩy lead từ "Contacted" sang "Working" để đảm bảo không có lead nào bị trì trệ ở giai đoạn đầu.
- Tiếp tục triển khai SLA phản hồi lead — mục tiêu liên hệ trong vòng 24 giờ kể từ khi tạo.
- Xem xét 35 lead "New" để đảm bảo chúng được phân công và tương tác kịp thời, ngăn ngừa rò rỉ pipeline tiềm ẩn.

---

#### Phân Tích Đánh Giá Lead Theo Nguồn (Biểu Đồ Cột Xếp Chồng)

![Lead Rating Breakdown by Source](screenshots/rocc6_lead_rating_by_source.png)

| Nguồn Lead    | Nóng | Ấm  | Lạnh | Tổng  |
|---------------|-----|------|------|-------|
| Web           |  2  |  9   |  7   |  18   |
| Trade Show    |  4  |  6   |  4   |  14   |
| Advertisement |  3  |  7   |  7   |  17   |
| Partner       |  6  |  8   |  3   |  17   |
| Referral      |  3  |  8   |  4   |  15   |
| Cold Call     |  7  |  8   |  4   |  19   |
| Tổng          | 25  | 46   | 29   | 100   |

**Điểm Chính:**
**Cold Call tạo ra nhiều lead nhất (19)**, nhưng cũng có tỷ lệ cao lead Hot (7) và Warm (8), chỉ có 4 Cold. **Partner cũng nổi bật với 6 Hot và 8 Warm trên tổng 17**, *khiến nó trở thành nguồn tốt nhất cho lead chất lượng cao.* **Ngược lại, Web và Advertisement tạo ra nhiều lead Cold hơn (7 mỗi nguồn) và ít Hot hơn (2 và 3 tương ứng).** Biểu đồ này cho thấy không phải tất cả các kênh có lượng lớn đều mang lại chất lượng như nhau, và các nguồn dựa trên quan hệ (Partner, Referral) có xu hướng tạo ra nhiều lead sẵn sàng mua hơn.

**Hành Động Đề Xuất:**
- Tăng cường đầu tư vào kênh Partner và Cold Call — những kênh mang lại số lượng lead Hot và Warm cao nhất.
- Đánh giá lại đầu tư vào Web và Advertisement, tập trung cải thiện chất lượng lead hoặc nuôi dưỡng để tăng tỷ lệ chuyển đổi lead Hot.
- Với Referral, tìm cách tăng chuyển đổi lead Hot, vì nguồn này tạo ra nhiều lead Warm nhưng tương đối ít Hot.
- Tiếp tục theo dõi hiệu suất Trade Show, vì kênh này cung cấp hỗn hợp chất lượng lead cân bằng.

---

### HÀNG 4: Phân Tích Sâu Pipeline — Độ Tin Cậy Dự Báo và Giá Trị Theo Kênh

#### Độ Tin Cậy Giao Dịch: Góc Nhìn Pipeline (Biểu Đồ Ngang Xếp Chồng)

![Deal Confidence Pipeline View](screenshots/rocc7_deal_confidence.png)

| Danh Mục Dự Báo | Kinh Doanh Mới | Kinh Doanh Hiện Tại | Tổng      | % Pipeline Đang Mở |
|-------------------|--------------|-------------------|-----------|--------------------|
| Pipeline          |   ~$9.5M     |     ~$10.6M       |  ~$20.1M  |      ~46.4%        |
| Best Case         |   ~$8.6M     |     ~$7.6M        |  ~$16.2M  |      ~37.4%        |
| Commit            |   ~$5.3M     |     ~$1.8M        |  ~$7.1M   |      ~16.4%        |
| Tổng              |  ~$23.4M     |     ~$20M         |  ~$43.4M  |      ~100%         |

**Điểm Chính:**  
Chỉ 16.4% pipeline đang mở (~$7.1M) nằm trong danh mục "Commit" — đây là các giao dịch có độ tin cậy cao mà đội ngũ kỳ vọng sẽ đóng. Gần một nửa (46.4%, ~$20.1M) nằm trong danh mục "Pipeline" lỏng nhất, nghĩa là các giao dịch đó chưa được nâng lên vị trí dự báo mạnh hơn. Đây là tín hiệu về vệ sinh dự báo: hoặc các giao dịch thực sự ở giai đoạn đầu, hoặc nhân viên không cập nhật danh mục dự báo khi giao dịch tiến triển.

Tỷ lệ phân chia giữa Kinh Doanh Mới và Kinh Doanh Hiện Tại xấp xỉ $23.4M so với $20M, cho thấy sự cân bằng lành mạnh giữa tạo pipeline mới và cơ hội kinh doanh hiện tại. Tuy nhiên, có sự sụt giảm đáng kể ở giai đoạn Commit cho kinh doanh hiện tại (chỉ $1.8M so với ~$5.3M cho kinh doanh mới), điều này có thể cho thấy thách thức trong việc đóng gia hạn hoặc mở rộng. Ngoài ra, đối với kinh doanh hiện tại, có sự suy giảm mạnh từ Best Case ($7.6M) xuống Commit (~$1.8M), gợi ý rằng nhiều cơ hội gia hạn hoặc mở rộng đang bị trì hoãn trước khi đạt trạng thái đóng có độ tin cậy cao. Mẫu hình này cần được điều tra thêm để xác định và giải quyết các trở ngại trong việc đẩy giao dịch kinh doanh hiện tại qua các giai đoạn cuối.

**Hành Động Đề Xuất:**
- Yêu cầu nhân viên cập nhật danh mục dự báo ở mỗi bước chuyển giai đoạn — độ chính xác dự báo phụ thuộc vào phân loại nhất quán.
- Kiểm tra nhóm ~$20.1M "Pipeline": các giao dịch này thực sự ở giai đoạn đầu, hay một số đã tiến triển mà không được phân loại lại?
- Ưu tiên chuyển các giao dịch Best Case (~$16.2M) sang Commit thông qua sự tham gia của lãnh đạo, triển khai proof-of-concept, hoặc đẩy nhanh đàm phán.
- Điều tra giá trị Commit thấp cho kinh doanh hiện tại để xác định các trở ngại tiềm ẩn trong việc đóng gia hạn hoặc cơ hội upsell.

---

#### Giá Trị Pipeline Theo Nguồn Lead (Biểu Đồ Ngang)

![Lead Source Pipeline Value](screenshots/rocc8_lead_source_pipeline_value.png)

|  Nguồn Lead   | Giá Trị Pipeline |
|---------------|----------------|
| Referral      |     $10.4M     |
| Partner       |     $9M        |
| Advertisement |     $8.6M      |
| Cold Call     |     $8M        |
| Trade Show    |     $6.1M      |
| Web           |     $5.9M      |

**Điểm Chính:**
**Giao dịch từ nguồn Referral mang giá trị pipeline tổng lớn nhất ($10.4M)**, tiếp theo là Partner ($9M) và Advertisement ($8.6M). Cold Call cũng đóng góp đáng kể ($8M), trong khi Trade Show ($6.1M) và Web ($5.9M) tụt lại phía sau. Phân tích này cho thấy các kênh dựa trên quan hệ (Referral và Partner) là động lực chính của giá trị pipeline, nhưng các kênh kỹ thuật số và outbound (Advertisement, Cold Call) cũng đóng vai trò quan trọng.

Đáng chú ý, Advertisement vượt qua Cold Call và Web về tổng giá trị pipeline, cho thấy đầu tư marketing đang chuyển hóa thành cơ hội có giá trị cao hơn so với giả định trước đó. Web, mặc dù là nguồn lead phổ biến, tạo ra giá trị pipeline thấp nhất, cho thấy khoảng cách tiềm ẩn trong chuyển đổi hoặc đánh giá chất lượng.

**Hành Động Đề Xuất:**
- Bảo vệ và mở rộng chương trình Referral và Partner — đây vẫn là các nguồn có giá trị cao nhất theo tổng đóng góp pipeline.
- Tiếp tục đầu tư vào Advertisement, vì đây hiện là nguồn pipeline top ba và có thể mang lại tăng trưởng có thể mở rộng.
- Với Cold Call, tập trung cải thiện chất lượng lead để tối đa hóa giá trị cơ hội được tạo ra.
- Điều tra lý do Web ($5.9M) tạo ra giá trị pipeline thấp nhất mặc dù lượng lead có thể cao; giải quyết mọi vấn đề chuyển đổi hoặc bàn giao giữa marketing và sales.
- Xem xét ROI của Trade Show để xác định liệu giá trị pipeline có biện minh cho khoản đầu tư so với các kênh khác.

---

### HÀNG 5: Hiệu Suất Thị Trường & Đội Ngũ — Doanh Thu Theo Ngành và Năng Suất Nhân Viên

#### Ngành Hàng Đầu Theo Doanh Thu (Biểu Đồ Kết Hợp)

![Top Industries by Revenue](screenshots/rocc9_top_industries_by_revenue.png)

| Ngành | Số Tài Khoản | Doanh Thu TB Hàng Năm |
|---|---|---|
| Manufacturing | 5  | $31.4M |
| Consulting    | 16 | $31M   |
| Energy        | 12 | $31M   |
| Healthcare    | 11 | $30.2M |
| Finance       | 4  | $28.9M |
| Media         | 11 | $28.5M |
| Technology    | 6  | $27.7M |
| Real Estate   | 14 | $27.6M |
| Education     | 9  | $24.3M |
| Retail        | 12 | $22.8M |

**Điểm Chính:**
Biểu đồ này làm nổi bật cả khối lượng tài khoản và hiệu quả doanh thu theo ngành. **Consulting dẫn đầu với 16 tài khoản và doanh thu trung bình mạnh $31M**, khiến nó trở thành phân khúc lớn nhất và có giá trị nhất. **Real Estate (14 tài khoản, trung bình $27.6M)** và **Retail (12 tài khoản, trung bình $22.8M)** cũng là các phân khúc lớn, mặc dù Retail tụt lại về doanh thu trung bình. **Energy, Healthcare và Manufacturing đều có doanh thu trung bình cao ($30M+)**, trong khi **Media (trung bình $28.5M)** và **Technology (trung bình $27.7M)** thể hiện giá trị tốt trên mỗi tài khoản mặc dù khối lượng thấp hơn. Education có ít tài khoản hơn (9) và doanh thu trung bình thấp nhất ($24.3M).

Góc nhìn này thiết yếu cho lập kế hoạch lãnh thổ: các ngành dẫn đầu về khối lượng (Consulting, Real Estate, Retail) cần phủ sóng rộng, trong khi các ngành có ROI cao (Consulting, Energy, Manufacturing, Healthcare) mang lại lợi nhuận tốt nhất trên mỗi tài khoản.

**Hành Động Đề Xuất:**
- Ưu tiên mở rộng trong các ngành có ROI cao như Consulting, Energy, Manufacturing và Healthcare, nơi doanh thu trung bình trên mỗi tài khoản là cao nhất.
- Đảm bảo các ngành dẫn đầu về khối lượng (Consulting, Real Estate, Retail) có đủ nhân viên phụ trách để tối đa hóa cơ hội.
- Điều tra doanh thu trung bình thấp hơn của Retail và Education để xác định liệu các ngành này có xứng đáng tiếp tục tập trung hay nên chuyển nguồn lực sang các ngành có ROI cao hơn.

---

#### Ma Trận Hiệu Suất Nhân Viên (Biểu Đồ Cột Xếp Chồng)

![Rep Performance Matrix](screenshots/rocc10_rep_performance_matrix.png)

| Nhân Viên     | Số Giao Dịch | Tổng Giá Trị Pipeline | GT Giao Dịch TB |
|---------------|------------|----------------------|----------------|
| David Okafor  |     26     |       $13.9M         |     $533K      |
| Emily Watson  |     17     |       $8.4M          |     $494K      |
| Maria Garcia  |     13     |       $5.1M          |     $394K      |
| Rachel Kim    |     13     |       $6.8M          |     $526K      |
| Chris Nguyen  |     11     |       $6.9M          |     $625K      |
| James Patel   |      8     |       $4.5M          |     $565K      |
| Michael Torres|      8     |       $3.7M          |     $460K      |
| Sarah Chen    |      4     |       $1.4M          |     $350K      |

**Điểm Chính:**  
**David Okafor là người có hiệu suất nổi bật nhất** — 26 giao dịch với tổng giá trị pipeline $13.9M, nhiều hơn bất kỳ nhân viên nào khác. Emily Watson theo sau với 17 giao dịch và $8.4M. Cùng nhau, hai nhân viên này nắm giữ **43 trên 100 giao dịch (43%) và ~$22M tổng pipeline (44%)**. Điều này vừa ấn tượng vừa là rủi ro tập trung: nếu một trong hai không làm việc được, gần nửa pipeline sẽ không có người quản lý.

Ở đầu kia, ba nhân viên cuối (Sarah Chen, Michael Torres, James Patel) quản lý tổng cộng chỉ 20 giao dịch và ~$9.6M — có tiềm năng nhận thêm pipeline nếu khối lượng công việc được tái phân bổ.

Các phân đoạn xếp chồng cũng cho thấy phân bổ giai đoạn của mỗi nhân viên: sự kết hợp lành mạnh các giai đoạn cho thấy quản lý pipeline tích cực, trong khi tập trung ở giai đoạn đầu có thể cho thấy nhân viên đang xây dựng pipeline nhưng không đẩy nó tiến triển.

**Hành Động Đề Xuất:**  
- Nghiên cứu quy trình làm việc của David Okafor và Emily Watson — tốc độ và khối lượng giao dịch của họ khiến họ trở thành chuẩn mực nội bộ. Ghi lại quy trình đánh giá chất lượng, nhịp độ theo dõi, và cách chuyển từ discovery sang specification.
- Đánh giá cân bằng khối lượng công việc: Sarah Chen (4 giao dịch) và Michael Torres (8 giao dịch) có năng lực đáng kể. Cân nhắc phân phối lại lead hoặc tài khoản đến để cân bằng.
- Kiểm tra hồ sơ Chris Nguyen: mặc dù chỉ có 11 giao dịch, tổng $6.9M và giá trị giao dịch trung bình $625K cho thấy sự chọn lọc giao dịch giá trị cao. Nếu có chủ đích, đây là chiến lược chuyên môn hóa đáng được hỗ trợ.

---

## 🔑 Tóm Tắt Nhận Định Chiến Lược

| # | Nhận Định | Tác Động Kinh Doanh | Hành Động Đề Xuất |
|---|---|---|---|
| 1 | Pipeline mở $43.3M với tỷ lệ thắng 60% | Nền tảng pipeline mạnh; khả năng đóng giao dịch đã được chứng minh | Duy trì tiêu chuẩn đánh giá chất lượng; bảo vệ tỷ lệ thắng khi pipeline mở rộng |
| 2 | $13.4M (~28%) tích tụ ở giai đoạn Discovery | Giao dịch bị trì hoãn — khách hàng cần hỗ trợ tiến sang Specification | Hỗ trợ bán hàng tại bước chuyển Discovery → Specification; cung cấp playbook và công cụ xác định phạm vi |
| 3 | Chỉ ~16% pipeline nằm trong danh mục dự báo "Commit" | Độ chính xác dự báo có nguy cơ; đa số pipeline được phân loại lỏng | Bắt buộc cập nhật danh mục dự báo tại mỗi cổng giai đoạn |
| 4 | Referral là nguồn pipeline #1 theo giá trị ($10.4M) | Kênh dựa trên quan hệ thúc đẩy nhóm doanh thu lớn nhất | Mở rộng chương trình referral và partner; khuyến khích giới thiệu |
| 5 | Cold Call: lượng lớn (19 lead) nhưng chất lượng hỗn hợp | Cần tối ưu hóa chất lượng lead để phù hợp với khối lượng | Tập trung chiến lược Cold Call vào đánh giá chất lượng thay vì chỉ khối lượng |
| 6 | Retail và Education có doanh thu trung bình thấp nhất | Hiệu quả doanh thu thấp trên mỗi tài khoản ở các ngành này | Điều tra quy mô giao dịch; cân nhắc phân bổ lại phủ sóng sang ngành có ROI cao hơn |
| 7 | David Okafor + Emily Watson nắm 43% giao dịch và 44% pipeline | Rủi ro tập trung và cơ hội học hỏi thực tiễn tốt nhất | Ghi lại quy trình của người có hiệu suất cao; tái cân bằng khối lượng công việc để phát triển nhân viên khác |
| 8 | 35% lead vẫn ở trạng thái "New" | Chậm trễ tương tác có nguy cơ ảnh hưởng tạo pipeline | Triển khai SLA; tự động phân công lead Hot để tiếp cận ngay |

---

> *Dashboard này là một phần của dự án demo Salesforce RevOps. Tất cả dữ liệu là mẫu — không bao gồm thông tin thực từ khách hàng thực.*

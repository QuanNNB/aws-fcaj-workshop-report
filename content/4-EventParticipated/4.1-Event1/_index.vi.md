---
title: "Build-a-thon Kickoff - Code the Future with CMC Global"
date: 2026-09-26
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Báo Cáo Thu Hoạch Sự Kiện: “Build-a-thon Kickoff - Code the Future with CMC Global”

---

### 1. Thông Tin Tổng Quan Về Sự Kiện

| Mục | Chi Tiết |
| :--- | :--- |
| **Tên sự kiện** | **Build-a-thon Kickoff: Code the Future with CMC Global** |
| **Thời gian tổ chức** | Ngày 26 tháng 09 năm 2026 |
| **Hình thức tham gia** | Trực tiếp (Offline) tại hội trường sự kiện |
| **Đơn vị tổ chức** | **CMC Global** phối hợp cùng Cộng đồng Công nghệ Điện toán Đám mây AWS |
| **Vai trò tham gia** | Người tham dự (Attendee) & Thí sinh tiềm năng |

---

### 2. Thành Phần Diễn Giả & Chuyên Gia Chia Sẻ

* **Anh Trường** – *Tech Lead tại CMC Global*: Chịu trách nhiệm dẫn dắt kỹ thuật, chia sẻ chuyên sâu về giải pháp kiến trúc AI Bot tự động hóa xử lý sự cố xuyên múi giờ.
* **Chị Nhàn** – *Đại diện Phòng Marketing & Tuyển dụng CMC Global*: Giới thiệu tổng quan về bức tranh thị trường quốc tế, định hướng nghề nghiệp, văn hóa doanh nghiệp và ngày hội việc làm **CMC Job Fair**.

---

### 3. Mục Đích & Bối Cảnh Của Sự Kiện

1. **Khởi động sân chơi công nghệ Build-a-thon:** Tạo cơ hội cho các kỹ sư trẻ, thực tập sinh cọ xát với các bài toán chuyển đổi số thực tế của doanh nghiệp.
2. **Định hướng phát triển ứng dụng Cloud-Native & Generative AI:** Đưa ra các case study thực tế trong việc tích hợp các mô hình ngôn ngữ lớn (LLM) vào hệ thống vận hành.
3. **Mở rộng cơ hội nghề nghiệp (CMC Job Fair):** Cung cấp thông tin tuyển dụng, chương trình đào tạo Fresher/Intern và môi trường làm việc toàn cầu tại CMC Global.
4. **Lan tỏa kinh nghiệm thực chiến:** Chia sẻ cách các kỹ sư giải quyết bài toán vận hành hệ thống đa quốc gia khi gặp rào cản về múi giờ.

---

### 4. Nội Dung Chi Tiết & Case Study Kỹ Thuật Chuyên Sâu

#### 4.1. Giới thiệu về CMC Global & Ngày hội việc làm (CMC Job Fair)
* **Quy mô và thị trường quốc tế:** CMC Global hiện là một trong những doanh nghiệp công nghệ hàng đầu tại Việt Nam trong lĩnh vực cung cấp giải pháp và dịch vụ chuyển đổi số cho các thị trường lớn như **Úc, Nhật Bản, Hàn Quốc, Singapore, Châu Âu và Mỹ**.
* **Cơ hội cho Fresher/Intern:** Doanh nghiệp luôn chú trọng xây dựng lộ trình đào tạo bài bản cho các tài năng trẻ, tạo điều kiện tiếp cận các dự án quy mô lớn ngay từ giai đoạn đầu sự nghiệp.
* **Văn hóa làm việc linh hoạt & toàn cầu:** Môi trường đa văn hóa đòi hỏi kỹ sư không chỉ vững chuyên môn kỹ thuật mà còn phải linh hoạt trong giao tiếp và giải quyết bài toán đa múi giờ.

---

#### 4.2. Bài toán thực tế của doanh nghiệp: Rào cản lệch múi giờ với thị trường Úc
Trong phần chia sẻ kỹ thuật, anh Trường (Tech Lead) đã phân tích một bài toán vận hành mang tính sống còn mà CMC Global đối mặt:

* **Bối cảnh:** CMC Global chịu trách nhiệm vận hành và hỗ trợ kỹ thuật 24/7 cho các hệ thống phần mềm trọng yếu của đối tác và khách hàng lớn tại **Úc (Australia)**.
* **Vấn đề cốt lõi (Pain Point):** Múi giờ tại Úc đi trước Việt Nam từ 3 đến 4 tiếng. Khi các doanh nghiệp tại Úc bắt đầu giờ làm việc buổi sáng hoặc khi phát sinh sự cố khẩn cấp (P1/P2 Incidents), tại Việt Nam đang là rạng sáng hoặc ngoài giờ làm việc.
* **Hậu quả nếu xử lý thủ công:**
  * Thiếu hụt nhân sự on-call trực ca ban đêm để phản hồi ngay lập tức.
  * Tăng thời gian phản hồi trung bình (MTTA - Mean Time to Acknowledge), vi phạm cam kết chất lượng dịch vụ (SLA).
  * Khách hàng lo lắng khi hệ thống gặp lỗi mà không nhận được tín hiệu tiếp nhận hay chẩn đoán ban đầu từ đội ngũ hỗ trợ.

---

#### 4.3. Giải pháp kiến trúc: Xây dựng AI Incident Bot với Claude Kit & Slack Socket Mode
Để giải quyết triệt để bài toán trên mà không làm quá tải đội ngũ kỹ sư, nhóm kỹ thuật của CMC Global đã nghiên cứu và triển khai thành công một **Hệ thống Trợ lý AI tự động phản hồi và chẩn đoán sự cố**.

```mermaid
flowchart TD
    subgraph Australia["Đối tác & Khách hàng tại Úc"]
        User[Khách hàng / Hệ thống Alert] -->|Gửi tin nhắn báo lỗi| SlackChannel[Slack Incident Channel]
    end

    subgraph SecurityBoundary["Hạ tầng bảo mật nội bộ CMC Global"]
        SlackChannel <-->|WebSocket 2 chiều (Slack Socket Mode)| BotCore[AI Incident Bot Engine]
        BotCore -->|Truy vấn Context & Prompt| ClaudeKit[Custom Claude Kit Framework]
        ClaudeKit <-->|LLM Inference & Log Analysis| ClaudeAPI[Anthropic Claude Core Engine]
        ClaudeKit -->|System Persona / Soul Instructions| SoulConfig[Soul Persona Controller]
    end

    subgraph Operations["Đội ngũ Kỹ sư Việt Nam"]
        BotCore -->|Phản hồi sơ bộ tức thì| SlackChannel
        BotCore -->|Gửi báo cáo tóm tắt nguyên nhân gốc| Engineer[On-Call Engineers tại VN]
    end
```

Các thành phần kỹ thuật cốt lõi được áp dụng:

1. **Bộ công cụ tự phát triển (Custom Claude Kit):**
   - Đội ngũ kỹ sư CMC Global đã tự thiết kế một bộ thư viện bao đóng (wrapper framework) dựa trên **Claude API**.
   - Bộ kit này có nhiệm vụ quản lý vòng đời hội thoại, nén ngữ cảnh (context compression), định dạng dữ liệu đầu vào và kiểm soát chi phí token tối ưu khi tương tác với các mô hình Claude.

2. **Kỹ thuật kết nối an toàn với Slack Socket Mode:**
   - Thay vì sử dụng Webhook công khai truyền thống (yêu cầu phải mở port hoặc cấu hình IP public/NAT Gateway gây rủi ro an ninh), bot sử dụng **Slack Socket Mode**.
   - Cơ chế này duy trì một kết nối WebSocket bảo mật hai chiều từ bên trong hạ tầng máy chủ nội bộ ra ngoài Slack API, đảm bảo dữ liệu sự cố tuyệt đối không bị rò rỉ trên môi trường Internet công cộng.

3. **Thiết kế "Linh hồn" cho Bot (Soul / Persona Engineering):**
   - Định hình system instructions nghiêm ngặt giúp bot hoạt động như một kỹ sư hỗ trợ cấp cao: phong thái giao tiếp điềm tĩnh, chuyên nghiệp và có tính đồng cảm cao với khách hàng.
   - Bot được trang bị khả năng đọc hiểu log lỗi kỹ thuật, trích xuất mã lỗi, tra cứu cơ sở tri thức (Knowledge Base) nội bộ và đưa ra các khuyến nghị giảm thiểu rủi ro ban đầu (workaround) trong lúc chờ kỹ sư vào ca.

---

### 5. Kết Quả & Giá Trị Đạt Được Từ Sự Kiện

| Lĩnh Vực | Kết Quả Tiếp Thu Được |
| :--- | :--- |
| **Kỹ thuật công nghệ** | Hiểu rõ quy trình xây dựng AI Bot doanh nghiệp, cơ chế vận hành của **Slack Socket Mode** và cách tối ưu hóa LLM thông qua **Custom Kit**. |
| **Tư duy kiến trúc** | Nắm bắt phương pháp kết hợp công nghệ hiện đại để giải quyết bài toán vận hành đa quốc gia, giảm thiểu chi phí và tối ưu hóa SLA. |
| **Định hướng nghề nghiệp** | Hiểu rõ tiêu chí tuyển dụng của CMC Global, các kỹ năng cần trau dồi để tự tin ứng tuyển các vị trí Cloud / AI Engineer. |
| **Kỹ năng mềm** | Học hỏi phong cách trình bày kỹ thuật mạch lạc, gắn liền kiến trúc với bài toán kinh doanh từ các chuyên gia. |

---

### 6. Bài Học Rút Ra & Ứng Dụng Vào Đồ Án Thực Tập

1. **Tư duy Business-Centric:** Một giải pháp kỹ thuật tốt không nằm ở việc sử dụng công nghệ phức tạp nhất, mà nằm ở việc giải quyết chính xác nhất nút thắt vận hành của doanh nghiệp.
2. **Áp dụng vào Đồ án Workshop (Phần 5):** 
   - Lấy cảm hứng từ bài toán của CMC Global, tôi định hướng xây dựng một kịch bản ứng dụng trên **AWS** kết hợp giữa **Serverless (AWS Lambda, EventBridge, DynamoDB)** và **Generative AI (Amazon Bedrock / Claude)** để tự động hóa quy trình giám sát và thông báo sự cố.
3. **Bảo mật hạ tầng:** Chú trọng việc thiết kế các kết nối an toàn, hạn chế tối đa việc mở public endpoint ra ngoài Internet theo đúng chuẩn **AWS Well-Architected Framework (Security Pillar)**.

---

### 7. Hình Ảnh Ghi Nhận Tại Sự Kiện

{{% notice tip %}}
*Hình ảnh check-in rõ mặt và hình ảnh thực tế quá trình tham gia sự kiện Build-a-thon Kickoff cùng CMC Global:*
{{% /notice %}}

![Check-in trước Backdrop sự kiện](/images/4-event/checkin-backdrop.png)
*Hình 1: Check-in trước Backdrop sự kiện "Build-a-thon: Code the Future with CMC Global - AWS First Cloud Journey"*

![Diễn giả chia sẻ Slide kỹ thuật](/images/4-event/presentation-slide.png)
*Hình 2: Lắng nghe diễn giả trình bày về kiến trúc kỹ thuật: Slack Socket Mode, Claude Code và AWS*

![Không khí hội trường sự kiện](/images/4-event/event-venue.png)
*Hình 3: Check-in toàn cảnh hội trường cùng các bạn sinh viên và lập trình viên tham gia sự kiện*

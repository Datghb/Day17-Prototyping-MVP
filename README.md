# Day 17 — Main Studio v4  
# FlowLearn — Hypothesis & Cheaper Test Studio

## 1. Thông tin học viên

| Trường | Nội dung |
|---|---|
| Mã học viên | Day17-FlowLearn |
| Họ tên | FlowLearn Team Member |  Nguyễn Thành Đạt(2A202600944), Nguyễn Đăng Khương(2A202600584)
| Dự án đang làm | FlowLearn |
| Vai trò trong dự án | Frontend, product workflow, AI-assisted writing feedback validation |

---

## 2. Build-up Chain
ßß
| Hạng mục | Link / ghi chú |
|---|---|
| Day 16 artifact 02 | 02-jtbd-project-analysis.md |
| Present board / frame / file | Present board được gom trực tiếp trong README này |
| Nếu dùng chung board với dự án, phần của bạn nằm ở đâu? | Section FlowLearn - Day 17 Hypothesis & Cheaper Tests |

---

## 3. Công cụ dùng để làm studio này

| Câu hỏi | Nội dung |
|---|---|
| Công cụ dùng để làm studio này | Markdown + HTML-style wireframe mô phỏng trực tiếp trong README |
| Link present board / frame / file | Artifact đã được mô tả trực tiếp trong README, không cần mở file phụ |

---

# Bước 0 — JTBD Checkpoint

| Câu hỏi | Nội dung |
|---|---|
| Core JTBD hiện tại là gì? | Giáo viên Writing cần một cách nhanh hơn để thu bài, chấm bài, hiểu lỗi phổ biến của học sinh và quyết định buổi sau nên dạy gì. |
| Current workflow hiện tại là gì? | Giáo viên tạo đề, gửi đề hoặc link cho học sinh, học sinh viết bài, giáo viên thu bài, chấm thủ công từng bài, ghi nhận lỗi, sau đó tự tổng hợp để chữa bài trên lớp. |
| Pain step đau nhất là gì? | Giáo viên mất nhiều thời gian chấm từng bài và khó tổng hợp lỗi chung của cả lớp sau mỗi lần nộp bài. |
| AI leverage point nằm ở bước nào? | AI chen vào sau khi học sinh nộp bài: hỗ trợ phân tích lỗi, gom lỗi phổ biến, tạo báo cáo cá nhân/lớp và đề xuất nội dung buổi học tiếp theo. |
| Điểm còn mơ hồ nhất trước khi vào hypothesis | Chưa chắc giáo viên có thật sự cần báo cáo lỗi lớp học và sẵn sàng trả tiền cho tính năng này hay không. |

---

# Bước 1 — Chọn 1 Hypothesis Quan Trọng

| Câu hỏi | Nội dung |
|---|---|
| Hypothesis được chọn | Giáo viên IELTS/Writing sẵn sàng trả tiền cho FlowLearn nếu sản phẩm giúp họ tiết kiệm thời gian chấm bài và tự động tổng hợp lỗi phổ biến của cả lớp để biết buổi sau nên dạy gì. |
| Hypothesis này thuộc phần nào của dự án? | AI class report, teacher dashboard và next-lesson recommendation. |
| Nếu hypothesis sai thì chuyện gì sập / yếu đi? | Nếu giáo viên không cần hoặc không trả tiền cho class report, FlowLearn sẽ dễ bị xem như một AI essay grader bình thường, khó khác biệt với các công cụ đã có. |
| Vì sao chọn hypothesis này để làm bài hôm nay? | Vì đây là điểm khác biệt quan trọng nhất của FlowLearn. Thị trường đã có nhiều công cụ AI chấm Writing, nên FlowLearn cần chứng minh giáo viên cần một workflow dạy học theo dữ liệu, không chỉ cần điểm số AI. |

---

# Bước 2 — Current Approach Hiện Tại Của Dự Án

| Câu hỏi | Nội dung |
|---|---|
| Dự án đã từng làm / đang định làm gì để test hypothesis này? | Team đang định build web app có teacher dashboard, class management, create writing event, student writing room, submission list, AI feedback, class report và anti-cheat monitor. |
| Cách đó có cần build gì tương đối lớn không? | Có. Cần build frontend, backend, database, auth, API, AI pipeline, report UI, telemetry/anti-cheat và logic phân tích bài viết. |
| Cách đó tốn gì? | Tốn time, scope, design, code, data, API cost, AI prompt tuning và công sức test với giáo viên thật. |
| Vì sao cách hiện tại đang đắt hoặc chậm? | Team đang cố build gần như một sản phẩm hoàn chỉnh trước khi biết chắc giáo viên có thật sự cần class report và next-lesson recommendation hay không. |
| Câu hỏi muốn tự ép mình hỏi lại | Còn cách nào rẻ hơn để test hypothesis này không? |

---

# Bước 3 — Ít Nhất 3 Cách Rẻ Hơn Để Test Cùng Hypothesis

## Cách test A — Teacher Interview + Form

| Câu hỏi | Nội dung |
|---|---|
| Tên hướng test A | Teacher Interview + Form |
| Loại artifact | Interview script + form prototype |
| Người dùng sẽ thấy gì? | Giáo viên thấy một form khảo sát/phỏng vấn về workflow chấm Writing, pain point, nhu cầu báo cáo lớp và mức giá sẵn sàng trả. |
| Phía sau sẽ làm gì? | Team gửi form cho 5-10 giáo viên Writing hoặc phỏng vấn trực tiếp, sau đó tổng hợp câu trả lời để xem pain point có thật không. |
| Nó đang test hypothesis nào? | Giáo viên Writing sẵn sàng trả tiền nếu FlowLearn giúp tiết kiệm thời gian chấm bài và tổng hợp lỗi lớp học. |
| Vì sao rẻ hơn current approach? | Không cần build app, không cần backend, không cần AI pipeline. Chỉ cần form và cuộc phỏng vấn. |
| Nó giúp học được gì? | Biết giáo viên có gặp pain thật không, họ có quan tâm đến class report không, và mức giá 99k-199k/tháng có hợp lý không. |
| Nó chưa giúp học được gì? | Chưa kiểm tra được giáo viên có dùng sản phẩm thật trong lớp hay không. Chưa kiểm tra usability. |
| Artifact A nằm ở đâu? | Nằm trực tiếp ở phần Bước 4 của README này. |

---

## Cách test B — Mock Class Report

| Câu hỏi | Nội dung |
|---|---|
| Tên hướng test B | Mock Class Report |
| Loại artifact | Mocked output sample / report prototype |
| Người dùng sẽ thấy gì? | Giáo viên thấy một báo cáo mẫu sau khi 10 học sinh nộp bài: điểm trung bình, lỗi phổ biến, học sinh yếu gì và đề xuất buổi học tiếp theo. |
| Phía sau sẽ làm gì? | Team dùng 10 bài Writing mẫu, phân tích thủ công bằng ChatGPT/LanguageTool/manual, rồi tạo report giả lập. |
| Nó đang test hypothesis nào? | Giáo viên Writing sẵn sàng trả tiền nếu FlowLearn giúp họ hiểu lỗi của lớp và biết buổi sau nên dạy gì. |
| Vì sao rẻ hơn current approach? | Không cần build hệ thống thật. Chỉ cần tạo output mẫu để kiểm tra phản ứng của giáo viên với giá trị cốt lõi. |
| Nó giúp học được gì? | Biết giáo viên có thấy report hữu ích không, phần nào trong report quan trọng nhất, và họ có tin insight do AI tạo ra không. |
| Nó chưa giúp học được gì? | Chưa kiểm tra được tốc độ xử lý thật, độ chính xác AI trên dữ liệu lớn, và khả năng tự động hóa hoàn toàn. |
| Artifact B nằm ở đâu? | Nằm trực tiếp ở phần Bước 4 của README này. |

---

## Cách test C — Clickable Flow Demo

| Câu hỏi | Nội dung |
|---|---|
| Tên hướng test C | Clickable Flow Demo |
| Loại artifact | Click-through prototype / wireframe |
| Người dùng sẽ thấy gì? | Giáo viên thấy flow 4 màn hình: tạo bài Writing, học sinh làm bài, danh sách bài nộp, class report. |
| Phía sau sẽ làm gì? | Team dựng prototype tĩnh, chưa cần backend. Khi demo, team giả lập dữ liệu học sinh và báo cáo lớp. |
| Nó đang test hypothesis nào? | Giáo viên Writing sẵn sàng trả tiền nếu FlowLearn giúp workflow dạy Writing rõ ràng hơn và tiết kiệm thời gian chấm/tổng hợp lỗi. |
| Vì sao rẻ hơn current approach? | Không cần code app thật đầy đủ, không cần database, không cần authentication và không cần AI thật. |
| Nó giúp học được gì? | Biết giáo viên có hiểu flow không, có thấy workflow hợp lý không, và phần nào khiến họ muốn dùng thử. |
| Nó chưa giúp học được gì? | Chưa đo được hành vi sử dụng thật, chưa kiểm tra performance, chưa kiểm tra độ chính xác AI. |
| Artifact C nằm ở đâu? | Nằm trực tiếp ở phần Bước 4 của README này. |

---

# Bước 4 — Artifact Cho Cả 3 Cách

## Checklist artifact

| Cách | Đã có artifact chưa? | Artifact là gì? | Link / ảnh / frame |
|---|---|---|---|
| A | Rồi | Teacher Interview Form | Nằm trong README |
| B | Rồi | Mock Class Writing Report | Nằm trong README |
| C | Rồi | Clickable Flow Demo / Wireframe | Nằm trong README |

---

## Artifact A — Teacher Interview Form

### Mục tiêu test

Kiểm tra xem giáo viên Writing có thật sự gặp pain về chấm bài, tổng hợp lỗi lớp học, và có sẵn sàng trả tiền cho FlowLearn hay không.

### Prototype form

```text
FLOWLEARN TEACHER INTERVIEW FORM

1. Bạn đang dạy Writing cho nhóm nào?
[ ] IELTS Writing
[ ] TOEFL Writing
[ ] Academic Writing
[ ] Tiếng Anh phổ thông
[ ] Khác

2. Mỗi tuần bạn chấm khoảng bao nhiêu bài Writing?
[ ] Dưới 20 bài
[ ] 20-50 bài
[ ] 50-100 bài
[ ] Trên 100 bài

3. Trung bình bạn mất bao lâu để chấm 1 bài?
[ ] Dưới 5 phút
[ ] 5-10 phút
[ ] 10-20 phút
[ ] Trên 20 phút

4. Sau khi chấm bài, bạn có thường tổng hợp lỗi chung của cả lớp không?
[ ] Có, thường xuyên
[ ] Có, nhưng làm thủ công và khá mất thời gian
[ ] Thỉnh thoảng
[ ] Không

5. Bạn có muốn hệ thống tự chỉ ra "lớp đang yếu gì" không?
[ ] Rất cần
[ ] Có thể hữu ích
[ ] Chưa chắc
[ ] Không cần

6. Tính năng nào quan trọng nhất với bạn?
[ ] Chấm điểm theo rubric
[ ] Sửa lỗi grammar/vocabulary
[ ] Báo cáo lỗi của cả lớp
[ ] Gợi ý nội dung buổi học tiếp theo
[ ] Phát hiện hành vi làm bài bất thường

7. Nếu FlowLearn giúp tiết kiệm thời gian chấm bài và tạo báo cáo lớp,
   bạn sẵn sàng trả bao nhiêu mỗi tháng?
[ ] 0đ
[ ] 49.000đ
[ ] 99.000đ
[ ] 199.000đ
[ ] Trên 299.000đ

8. Bạn muốn FlowLearn cải thiện điều gì nhất?
Câu trả lời mở: ________________________________________
```

### Cách đọc kết quả

- Nếu phần lớn giáo viên chọn "Rất cần" hoặc "Có thể hữu ích", hypothesis có tín hiệu tích cực.
- Nếu nhiều giáo viên chọn mức 99.000đ-199.000đ/tháng, có tín hiệu willingness to pay.
- Nếu giáo viên chỉ quan tâm "AI chấm điểm" mà không quan tâm "class report", định vị của FlowLearn cần chỉnh lại.

---

## Artifact B — Mock Class Writing Report

### Mục tiêu test

Kiểm tra xem giáo viên có thấy báo cáo lớp học hữu ích không, đặc biệt là phần lỗi phổ biến và đề xuất buổi dạy tiếp theo.

### Mock output

```text
FLOWLEARN CLASS WRITING REPORT

Topic: Environmental Problems
Class: IELTS Writing Evening Class
Number of students: 10
Submissions: 10/10
Average band estimate: 5.8

------------------------------------------------------------
1. CLASS OVERVIEW
------------------------------------------------------------

Task Response:                5.8 / 9.0
Coherence & Cohesion:         6.2 / 9.0
Lexical Resource:             5.5 / 9.0
Grammar Range & Accuracy:     5.2 / 9.0

Main class weakness:
Most students understand the topic, but their opinion is not clearly expressed
in the introduction. Many essays lack specific examples and repeat simple vocabulary.

------------------------------------------------------------
2. COMMON MISTAKES
------------------------------------------------------------

| Error type                    | Students affected | Example                                  |
|------------------------------|-------------------|------------------------------------------|
| Thesis statement unclear      | 7/10              | "I think environment is important."     |
| Weak or general examples      | 6/10              | "People should protect nature."         |
| Subject-verb agreement        | 5/10              | "People has many problems."             |
| Overused linking words        | 4/10              | Repeated use of "Moreover"              |

------------------------------------------------------------
3. STUDENT SNAPSHOT
------------------------------------------------------------

| Student | Band | Main weakness           | Suggested teacher action       |
|---------|------|-------------------------|--------------------------------|
| Anh     | 6.0  | Examples too general    | Give model examples            |
| Bình    | 5.5  | Grammar accuracy        | Grammar correction task        |
| Chi     | 6.5  | Lexical variety         | Vocabulary upgrade task        |
| Dũng    | 5.0  | Essay structure         | Paragraph planning practice    |

------------------------------------------------------------
4. NEXT LESSON RECOMMENDATION
------------------------------------------------------------

Recommended lesson:
How to write a clear thesis statement for IELTS Discussion Essay.

Suggested activities:
1. Show 3 weak thesis statements from student essays.
2. Ask students to rewrite them into stronger versions.
3. Compare weak vs strong examples.
4. Give a 10-minute mini writing task.
```

### Câu hỏi hỏi giáo viên sau khi xem report

1. Report này có giúp thầy/cô biết buổi sau nên dạy gì không?
2. Phần nào hữu ích nhất: điểm số, lỗi phổ biến, student snapshot hay lesson recommendation?
3. Thầy/cô có tin insight này nếu biết AI tạo ra nhưng giáo viên có thể review lại không?
4. Nếu report này được tạo tự động sau mỗi bài Writing, thầy/cô có trả 99.000đ-199.000đ/tháng không?

---

## Artifact C — Clickable Flow Demo / Wireframe

### Mục tiêu test

Kiểm tra xem giáo viên có hiểu flow của FlowLearn không và có thấy workflow này hợp lý cho lớp Writing không.

### Wireframe flow

```text
SCREEN 1 — TEACHER CREATE WRITING EVENT

[FlowLearn Teacher Dashboard]

Event title:
IELTS Writing Task 2 - Environment

Writing prompt:
Some people believe that environmental problems are too big for individuals to solve,
while others think individual action is important. Discuss both views and give your opinion.

Rubric:
[IELTS Writing Task 2 Rubric]

Time limit:
[40 minutes]

Anti-cheat settings:
[x] Detect tab switching
[x] Detect copy/paste
[x] Track focus loss
[ ] Lock full screen mode

[Generate Student Link]
```

```text
SCREEN 2 — STUDENT WRITING ROOM

[FlowLearn Student Writing Room]

Prompt:
Some people believe that environmental problems are too big for individuals to solve,
while others think individual action is important.

Timer:
32:15 remaining

Essay editor:
In modern society, environmental problems are becoming more serious...

Integrity Monitor:
Tab switch: 2 times
Copy/paste: 0 times
Focus lost: 1 time
Typing pattern: Normal

[Submit Essay]
```

```text
SCREEN 3 — TEACHER SUBMISSION LIST

[Submission List]

| Student | Status    | Band estimate | Integrity        | Main issue             |
|---------|-----------|---------------|------------------|------------------------|
| Anh     | Submitted | 6.0           | Clean            | Examples too general   |
| Bình    | Submitted | 5.5           | 2 tab switches   | Grammar accuracy       |
| Chi     | Submitted | 6.5           | Clean            | Lexical variety        |
| Dũng    | Submitted | 5.0           | Paste detected   | Essay structure        |

[View Class Report]
```

```text
SCREEN 4 — CLASS REPORT

Class average: 5.8
Most urgent lesson: Thesis statement
Teacher time saved: approximately 2 hours

Next Lesson Recommendation:
Lesson focus: How to write a clear thesis statement for IELTS Discussion Essay.

Suggested activities:
1. Show weak thesis statements from student essays.
2. Ask students to rewrite them.
3. Compare weak vs strong examples.
4. Give a 10-minute mini writing task.

[Export Lesson Plan]
```

### Câu hỏi hỏi giáo viên sau khi xem flow

1. Flow này có giống cách thầy/cô đang dạy Writing không?
2. Màn hình nào tạo cảm giác hữu ích nhất?
3. Có bước nào thầy/cô thấy thừa hoặc khó hiểu không?
4. Nếu chỉ giữ 1 tính năng để trả tiền, thầy/cô sẽ giữ tính năng nào?

---

# Bước 5 — So Sánh Nhanh 3 Cách

| Tiêu chí | Cách A — Interview/Form | Cách B — Mock Report | Cách C — Clickable Flow Demo |
|---|---|---|---|
| Nhanh hơn current approach ở đâu? | Nhanh nhất, chỉ cần hỏi giáo viên. | Nhanh vì chỉ cần tạo report mẫu. | Nhanh hơn build app thật vì chỉ dựng UI tĩnh. |
| Rẻ hơn current approach ở đâu? | Không cần code, không cần AI. | Không cần backend, không cần AI automation. | Không cần database, auth, API, AI thật. |
| Gần với hành vi thật tới đâu? | Thấp - chủ yếu là ý kiến. | Trung bình - giáo viên thấy output gần thật. | Trung bình-cao - giáo viên thấy flow gần sản phẩm thật. |
| Học được điều gì rõ nhất? | Pain point và willingness to pay. | Giá trị của report và trust với AI insight. | Usability, comprehension và workflow fit. |
| Giới hạn lớn nhất là gì? | Người dùng có thể nói thích nhưng chưa chắc dùng. | Output mẫu có thể đẹp hơn sản phẩm thật. | UI demo chưa chứng minh nhu cầu trả tiền thật. |

## Chốt nhanh

| Câu hỏi | Trả lời |
|---|---|
| Trong 3 cách này, cách nào nhìn thuyết phục nhất khi present? | Cách B - Mock Class Report, vì nó cho thấy rõ giá trị khác biệt của FlowLearn: từ bài viết biến thành insight dạy học. |
| Trong 3 cách này, cách nào dễ bị lớp phản biện nhất? | Cách A - Interview/Form, vì giáo viên có thể trả lời tích cực nhưng hành vi thật chưa chắc giống câu trả lời. |

---

# Bước 6 — Gom Lại Thành Present Board Cá Nhân

Board present gồm 5 khối và đã được gom trực tiếp trong README này:

1. Hypothesis
2. Current approach hiện tại của dự án
3. Cheaper test A - Teacher Interview + Form
4. Cheaper test B - Mock Class Report
5. Cheaper test C - Clickable Flow Demo

| Câu hỏi | Nội dung |
|---|---|
| Bạn đã gom đủ 5 khối lên board chưa? | Rồi |
| Ảnh / screen / artifact nào quan trọng nhất khi present? | Mock Class Writing Report, vì nó thể hiện rõ FlowLearn khác AI essay grader bình thường ở điểm class-level insight và next-lesson recommendation. |
| Chỗ nào trên board đang bị dài chữ quá? | Phần current approach và giới hạn của từng test có thể rút gọn khi nói, nhưng vẫn giữ đầy đủ trong README để người chấm đọc được. |

---

# Bước 7 — Present Cá Nhân

## Luồng present 3-4 phút

| Phần | Thời lượng gợi ý | Nội dung |
|---|---:|---|
| 1 | 20-30s | JTBD checkpoint: giáo viên Writing cần thu bài, chấm bài, hiểu lỗi lớp và quyết định buổi sau nên dạy gì. |
| 2 | 20-30s | Hypothesis: giáo viên sẵn sàng trả tiền nếu FlowLearn tiết kiệm thời gian chấm và tạo class report hữu ích. |
| 3 | 30-45s | Current approach: build app đầy đủ đang quá to, tốn frontend/backend/database/AI pipeline. |
| 4 | 90s | Đi qua 3 cách test: interview form, mock class report, clickable demo. |
| 5 | 30-45s | So sánh trade-off: A rẻ nhất, B thể hiện value rõ nhất, C gần sản phẩm thật nhất. |
| 6 | 20-30s | Xin lớp phản biện vào câu hỏi: giáo viên có thật sự trả tiền cho class report không? |

## Chuẩn bị trước khi present

| Câu hỏi | Nội dung |
|---|---|
| Bạn sẽ mở link / frame nào khi present? | README này |
| Bạn muốn lớp phản biện mạnh nhất vào chỗ nào? | Hypothesis về willingness to pay và việc giáo viên có thật sự cần class-level report không. |
| Nếu chỉ có 30 giây để mở đầu, bạn sẽ nói câu gì? | FlowLearn không chỉ là AI chấm Writing; hypothesis hôm nay là giáo viên sẽ trả tiền nếu hệ thống giúp họ tiết kiệm thời gian chấm bài và biết buổi sau nên dạy gì dựa trên lỗi của cả lớp. |

## Câu hỏi muốn lớp phản biện

1. Giáo viên có thật sự cần class report và next-lesson recommendation, hay chỉ cần AI chấm từng bài?
2. Mức giá 99.000-199.000đ/tháng cho giáo viên cá nhân có hợp lý không?

---

# Bước 8 — Ghi Lại Sau Present

| Câu hỏi | Nội dung |
|---|---|
| Phản biện quan trọng nhất vừa nhận là gì? | Phần này sẽ được ghi sau buổi present. Trước buổi present, phản biện cần tập trung vào willingness to pay và sự khác biệt của FlowLearn so với AI essay grader. |
| Trong 3 cách test, cách nào bị hỏi nhiều nhất? | Dự kiến Cách B - Mock Class Report sẽ bị hỏi nhiều nhất vì đây là artifact thể hiện giá trị cốt lõi. |
| Cần chỉnh gì trên board / artifact? | Có thể cần rút ngắn chữ khi trình bày và làm rõ hơn cách đo kết quả interview/form. |
| Điều muốn giữ nguyên sau phản biện | Giữ hypothesis tập trung vào teacher workflow, class-level insight và next-lesson recommendation thay vì chỉ tập trung vào AI chấm điểm. |

---

# Chốt Trước Khi Nộp

- [x] Tôi đã checkpoint lại JTBD
- [x] Tôi đã chọn đúng 1 hypothesis
- [x] Tôi đã ghi lại current approach hiện tại của dự án
- [x] Tôi đã nghĩ ra ít nhất 3 cách rẻ hơn để test cùng hypothesis đó
- [x] Tôi đã làm artifact cho cả 3 cách
- [x] Tôi đã gom thành present board
- [x] Tôi đã chuẩn bị xong phần present cá nhân
- [x] Tôi đã chuẩn bị phần ghi lại sau present

---

# Nếu có 60 giây để chốt lại

1. FlowLearn đang test hypothesis: giáo viên Writing sẵn sàng trả tiền nếu hệ thống giúp tiết kiệm thời gian chấm bài và tổng hợp lỗi lớp để biết buổi sau nên dạy gì.
2. Current approach đang đắt/chậm vì team định build gần như full app trước khi xác thực nhu cầu thật.
3. Ba cách rẻ hơn là: Teacher Interview Form, Mock Class Report và Clickable Flow Demo.
4. Artifact của 3 cách cho thấy có thể test cùng một hypothesis mà chưa cần build sản phẩm hoàn chỉnh.

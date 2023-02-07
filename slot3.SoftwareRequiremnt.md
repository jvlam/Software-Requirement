CV
- thông tin cá nhân
- GPA
    - điểm trung bình tích lũy : là điểm tất cả các môn đã đậu chia trung bình 
    - Fsoft 
        - tùy từng kì khác nhau. GPA >= 8, mặc định được nhận thực tập, không qua p/v luôn, được lên làm dự án thật, lương luôn
        - dưới 8, bình thường, vào 1 phòng training, bắt nghiên cứu gì đó, báo cáo -> vào vòng p/v
            - passed: lên làm dự án
            - failed: ngồi FA tiếp, được huấn luyện, chờ, pv 
        
        - tránh làm những công ty lớn hơn 40h, đc nghỉ 2 ngày cuối tuần 
        - các công ty bắt đầu từ 8h-9h30
        - thời gian tính cả thời gian đi vs :))) 


- Skills
    - hard
    - solf
- Certificate
- Experiences
- Project 

# R/E REQUIREMENTS ENGINEERING - SOFTWARE REQUIREMENTS -SWR302
- học các kĩ thuật để tìm ra yêu cầu phần mềm. Phần mềm được viết theo nhu cầu, yêu cầu của ai đó. Ai đó có thể là: công ty, phân xưởng, tổ chức
quán ăn, khách sạn, ...
- Quy ước viết tắt:
- Requirements: REQs. reqs
- Project: prj
- Product: prod
- Manager: mgr
- Management: mgt
- Product Owner: PO
- Project Manager: PM
- IT BA:BA
- Developer: dev  

# I. REQUIREMENTS ENGINEERING  - 3E
- ["giải thích khái niệm một số thuật ngữ"]()
- ENGINEER
    - kĩ sư 
- ENGINE
    - động cơ 
- ENGINEERING
    - thông số kĩ thuật cân chỉnh máy móc
    - các bước thao tác, các vấn đề về kỹ thuật máy móc 
- ["Ví Dụ Về Sofeware Requirements"]()
    - tôi muốn app quản lý hoạt động quản lý của bệnh viện chợ rẫy 
    - tôi muốn app lưu được hồ sơ bệnh nhân và quá trình thăm khám và điều trị  -> ["functional requirements"]()
    - app thu ngân -> tính năng tạo mới đơn hàng và tích điểm -> tạo mới hồ sơ khách hàng thân thiết (cskh) 
    - app hỗ trợ tối đa 10k user cùng lúc xài app ở lúc cao điểm săn sale -> ["non-functional requirements"]()
    - app response trong vòng <= 3s 
- ["Tại Sao Lại Phải học các kỹ thuật tìm REQs"]()
    - tam sao thất bổn, các thành viên của dev team không hiểu ý nhau 
    - không diễn đạt rõ được điều mong muốn
    - REQS bị thay đổi 
    - REQS mâu thuẫn nhau 
    - không diễn đạt chính xác mong muốn của họ 
    - ảnh hưởng lớn đến việc chỉnh sửa REQS
    - tỉ lệ sai sót khi làm REQS cao, phí tổn fix cao 
- ["SCOPE OF REQUIREMENT"]()
    - R/E tập trung vào những điều gì, 3 góc nhìn về R/E tìm ra REQ thì tập trung vào điều gì ?
        - WHY : tại sao lại cần làm cái app này ?
        - WHAT: APP sẽ có những màn hình gì, chức năng gì ?
        - WHO : ai, thiết bị gì (quét sp để nhận diện thanh toán), hệ thống nào khác(momo để thanh toán) sẽ tham gia vào việc vận hành app ?



## 3. PROJECT MANAGER vs PRODUCT MANAGER
- PRODUCT MANAGER - giám đốc sp
    + tập trung vào product, tìm requirements, cải tiến app 
    + CHỊU TRÁCH NHIỆM TÌM RA TÍNH NĂNG, WHAT/WHO 
- PROJECT MANAGER - quản lý dự án 
    + scope
    + budget
    + time
    + QUẢN LÝ DỰ ÁN TRÊN TAM GIÁC VÀNG 

# II. VÍ DỤ VỀ REQS

# III. WHY R/E TẠI SAO CẦN HỌC VỀ CÁC KĨ THUẬT TÌM KIẾM YÊU CẦU PHẦN MỀM ?

# IV. CÁC KHÁI NIỆM DỄ GÂY NHẦM LẪN, CẦN PHÂN BIỆT RÕ HƠN
- ["Một Số Thuật Ngữ Cần Phân Biệt"]()
    - 1. AS-IS SYSTEM  vs TO-BE SYSTEM 
            - ["AS-IS SYSTEM"]() - LEGACY - HIỆN TRẠNG
                - cách thưc hiện nay cá doanh nghiệp | cá tổ chức |  khách hàng đang làm công việc của họ đang làm bằng tay hay làm 1 cái app đang dùng 
            - ["TO-BE SYSTEM"]() 
                - app mới mình đang sẽ làm để thay thế app cũ, hiện trạng cũ 
            - <kbd>final</kbd> công ty phần mềm convert từ legacy -> tobe 

    - 2. PRODUCT VS PROJECT
            - ["PRODUCT"]() - product manager, po, ba, brSE 
                - ["kết quả"]() hoàn tất một project - production 
                - tập trung vào tính năng - WHAT, WHO 

            - ["PROJECT"]() - project manager PM
                - ["quá trình"]() làm ra 1 sản phầm mềm, 1 product   - development
                - BUGET, TIME, SCOPE, HR, QUALITY (golden triangle of project manegement)

# VI. PHẦN MỀM VÀ NƠI TÌM RA CHÚNG 
- ["App Và Nơi Xuất Thân Của Chúng, App Xuất Hiện Như Thế Nào"]()
    1. đến từ cty công nghệ (dùng app tự viết để dùng trong mô hình kinh doanh) - phụ thuộc 100% vào mô hình kinh doanh 
        + Grab, bee, baemin, momo, lazada 
        + dành cho số đông người dùng, bá tánh thiên hạ -> app này gọi là : ["GENERIC APP"](), PRODUCT 
        + Nhận yêu cầu phần mềm, các chức năng code từ ["PO"], ["PROD MGR"]() 
    * ưu nhược điểm 
        + Dev ko có danh phận cao
        + Biết rất sau 1 (vài) loại app 

    2. các công ty khác, dùng phần mềm phục vụ cho hoạt động nội bộ hay kinh doanh 
        + Ví Dụ: TPBank, ACB, Bảo hiểm nhân thọ (Prudential), TGDD, Novaland, BeerSG, siêu thị lớn như CoopMart, BigC, HAGL 
        * Đặc trưng của dân dev
            - Dân dev nhận yêu cầu về phần mềm từ ["PO"], ["Prod Mgr"]() cho cái app làm cho bá tánh xài
                - eBaking, thegioididong.com, ATM, app CoopMart để mua hàng siêu thị giao tận nhà 
            - Dân dev nhận yêu cầu về phần mềm từ ["BA"] cho cái app mà làm riêng cho nội bộ cty xài, nhân viên công ty xài 
                - app quản lý tài khoản ATM, 
                - app này được viết theo nhu cầu các nhân viên, để giúp họ làm các công việc của cty, hiệu quả hơn 
                - Để làm app này BA phải đi hỏi các nhân viên, anh chị đang làm thu ngân tính tiền ra sao, em sẽ độ ra phần mềm ngon giúp anh chị

- CHỐT HẠ 
    + BA sẽ là gã giao tiếp trực tiếp với các user/khách hàng/người đặt hàng cụ thể để hiểu họ muốn tính năng gì, như thế nào - phân tích nghiệp vụ khách hàng
    + PO, PROD MGR là gã nhìn xung quanh, nhìn đối thủ, tưởng tượng tính năng phần mềm sẽ phục vụ cho số đông người dùng 
- DÙ LÀ GÃ NÀO THÌ CŨNG: TÌM RA CÁC TÍNH NĂNG, CÁC TÍNH NĂNG, CÁC YÊU CẦU, CÁC MÀN HÌNH


    3. công ty thuần IT, cty làm phần mềm - LÀM APP ĐỂ KIẾM TIỀN
        + Fsoft, KMS, NashTech ...
        + Nhân viên chủ lực của các công ty này chính là DEV - CÓ DEV DANH PHẬN 
        * Đặc trưng của dân dev
            - Dân dev nhận yêu cầu phần mềm từ PO, PROD MGR 
        - 3.1
        - 3.2 CÁC CÔNG TY LÀM DỊCH VỤ - SERVICE-BASE, AI ĐẶT HÀNG LÀM PHẦN MỀM 
            - Dân Dev nhận yêu cầu phần mềm từ các khách hàng cụ thể như liệt kê ở trên và ta phải làm app theo đúng cách AS IS SYSTEM  

- CHỐT HẠ 
    + BA, BrSE, PO, PROD MGR đều cũng làm việc với REQUIREMENTS
    REQS CÓ THỂ ĐẾN TỪ AI KHÁC NÓI, HOẶC TỰ TƯỞNG TƯỢNG HOẶC KHẢO SÁT THỊ TRƯỜNG HOẶC ĐỐI THỦ

- CÔNG TY LÀM PRODUCT: TỰ BỎ TIỀN TÚI RA ĐỂ LÀM APP VÀ HY VỌNG THIÊN HẠ SẼ TRẢ TIỀN XÀI APP -> TRẢ NHIỀU, THÍCH XÀI -> CÓ 1 ĐẾ CHẾ 
- CÔNG TY LÀM SERVICE-BASE/OUTSOURCE :
    - CÓ NGƯỜI BỎ TIỀN CHO MÌNH LÀM APP, MÌNH KH PHẢI LO ĐI BÁN APP
    - CẦN CÓ SỐ MÁ ĐỂ NGƯỜI TA GỬI TIỀN CHO MÌNH LÀM APP CHO HỌ 

    4. CÔNG TY START-UP TRONG CÔNG NGHỆ
    * VÍ DỤ: ELSA
    - bạn có ý tưởng độc đáo, chưa có trên thị trường, bạn sẽ hùn vốn, vay vốn kêy gọi đầu tư SHARK hỗ trợ và hy vọng thành công 
    - BẠN ĐÓNG VAI TRÒ QUAN TRỌNG NHẤT, OÁCH NHẤT: FOUNDER
    - BẠN ĐÓNG VAI PO/PROD MGR
    - KHỞI NGHIỆP LÀM APP CHO BÁ TÁNH 

# II. PHÂN LOẠI REQUIREMENTS: 
    
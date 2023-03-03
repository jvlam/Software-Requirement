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

# VII. PHÂN LOẠI REQUIREMENTS: 

* CHỐT HẠ 
- Có nhiều loại công ty cùng tuyển dụng Developer: cty công nghệ, công ty lớn, công ty thuần IT (product-based, service-based/outsourcing)
- Nhưng chỉ ở công ty thuần IT thì dev mới có danh phận !!!
- App mà được viết hướng về bá tánh đám đông người dùng thì gọi là generic app, product
- App mà được viết theo đơn đặt hàng riêng của cty nào đó/phòng ban nào đó và dùng trng nội bộ hoạt động của họ, app làm theonhu cầu riêng, gọi CUSTOM, CUSTOMIZEED APP, BESPOKE APP
- Những job title, những job position: BA, BRSE, PO, PRODUCT MANAGER ĐỀU LÀ NHỮNG GÃ ĐƯA RA REQUIREMENTS
- REGS có thể đến từ thiên hạ
- REQS có thể đến từ 1 ai đó cụ thể nói ra: bác sĩ, thu ngân, thủ kho, thủ thư, ông chủ quán ăn 

- Requirements là 1 câu phát biểu - a statement từ ai đó khác làm!!! 
   A-------------yêu cầu----------------B làm điều gì đó
            a statement
- Trong làm phần mềm thì có 2 loại yêu cầu : 
1. ["PROJECT REQUIREMENTS"]()  
- Định Nghĩa: là những câu phát biểu đề cập/mô tả đến việc Quản Lí Dự Án và người PM phải có trách nhiệm hoặc đặt ra, hoặc phải xử lí
* Ví Dụ:
- Tuần này anh em tăng ca (OT) để kịp tiến độ 
- Cần phải mua máy đọc barcode cầm tay để hiện thực tính/coding năng TẠO MỚI ĐƠN HÀNG 
- Cần mua camera độ phân giải cao để code tính năng GỬI XE, LẤY XE của app Bãi xe thông minh 

2. ["PRODUCT REQUIREMENTS"]()
- Định Nghĩa: là nhưng câu phát biểu từ ai đó để yêu cầu nhóm dev hiện thực/viết code cho tính năng/màn hình mà khách hàng trông đợi để sử dụng
- Là câu phát biểu về chức năng, tính năng, tên gọi màn hình mà app sẽ cần cung cấp!!!
- GÓC NHÌN WHAT, WHO, (WHY)
- môn học SWR , BA, BrSE, PO Product Owner SẼ TẬP TRUNG VÀO CÁI PRODUCT REQS KO TẬP TRUNG VÀO PROJECT REQS
* CHIA PRODUCT REQS THÀNH 3 LOẠI NHỎ HƠN
    + ["BUSINESS REQS"]()
    + ["USER REQS"]()
        * Định Nghĩa: Là những câu phát biểu từ phía người sẽ dùng app, người đặt hàng làm app, những câu phát biểu dễ hiểu, ko dùng thuật ngữ kĩ thuật.
        - Là những câu phát biểu ở góc nhìn người dùng, về cái tính năng, chức năng, cái tên, màn hình của cái app đang làm mà tương lai họ sẽ sử dụng trong công việc của họ 
        * Ví Dụ: 
        - App QLBV: Bác sĩ nói: 'Tôi muốn app giúp lưu trữ hồ sơ bệnh nhân mà hiện nay đang dùng = giấy + excel'
        - App Thu ngân của tiệm trà sữa : chủ tiệm trà sữa nói rằng ...
        # USER REQUIREMENTS NẾU PHÁT BIỂU ĐẦY ĐỦ BAO GỒM TÊN TÍNH NĂNG/TÊN MÀN HÌNH KÈM AI XÀI NÓ CHO MỤC ĐÍCH GÌ, THÌ TA GỌI NÓ LÀ : USER STORY
        - CÁCH VIẾT USER STORY NGHIÊM NGẶT HƠN USER REQS, MẶC DÙ LÀ 1 USER STORY DÙNG TRONG PHƯƠNG PHÁP AGILE 
        - AS A <ROLE> I WANT TO <WHAT> SO THAT <PURPOSE>


    + ["SYSTEM REQS"]()
        * Định Nghĩa: CONVERT TỪ USER REQUIREMENTS
        - là câu phát biểu mổ tả tính năng phần mềm/chức năng phần mềm/tên màn hình
          nhưng chi tiết hơn câu User Reqs, nó mang yếu tố kĩ thuật, yếu tố lập trình vào > người đọc câu này là dev team 
        
        - App QLBV: 
            - Bác sĩ nói: 'Tôi muốn app giúp lưu trữ hồ sơ bệnh nhân mà hiện nay đang dùng = giấy + excel'
            - App có tính năng lưu trữ hồ sơ bệnh nhân. Hồ sơ bệnh nhân có những infor cơ bản sau, tên bn, năm sinh, địa chỉ, sdt
            mã số bệnh nhân theo định dạng: <yyyy><mm><xxxx>
            - ví dụ: 20230212345 > SYSTEM REQUIREMENT 


        - lại chia nhỏ thành 2 loại nhỏ hơn
            - FUNCTIONAL REQUIREMENTS
                * Định nghĩa: là những câu phát biểu tính năng phần mềm/tên màn hình/góc nhìn chi tiết/ góc nhìn của dev để cung cấp khả năng giúp cho công việc
                của user/khách hàng, giúp khách hàng/user làm điều gì đó
                WHAT, VERB PHẢN ÁNH TÍNH NĂNG CỦA APP GIÚP USER LÀM ĐIỀU GÌ
                * Ví Dụ: App có tính năng lưu trữ hồ sơ bệnh nhân. Hồ sơ bệnh nhân có những info cơ bản sau, tên bn, năm sinh, địa chỉ, số điện thoại, dị ứng ...
                mã số bệnh nhân theo định dạng : <yyyy><mm><xxxxx>
                - ví dụ: 20230212345 > SYSTEM REQUIREMENT 
            - NON-FUNCTIONAL REQUIREMENTS 
                * Định nghĩa: Những câu phát biểu nói về cảm giác, cảm xúc trải nghiệm app của user hay những ràng buộc mà app cần phải thỏa 
                - Thường nó sẽ dùng tính từ để mô tả tính chất hoạt động của toàn bộ app, ko focus đề cập vào 1 tính năng cụ thể nào đó 
                - Có thể tóm gọn yêu cầu phi chức năng đc phát biểu qua những cụm từ 'nhanh/chậm/đã/to/nhỏ/đẹp/xấu/tuân thủ/bảo mật'
                * Ví Dụ: 
                    - App phải dễ dùng
                    - App kế toán nhân sự

# VIII. STAKE-HOLDER 
- Để làm một dự án phần mềm sẽ có rất nhiều người có liên quan cùng tham gia. Bao gồm phía cty phần mềm và bên đặt hàng làm app 
    + 1. DEVELOPMENT TEAM
    + 2. BA IT, BRSE, PRODCUT OWER, PROJECT MANGAFER 
    + 3. CUSTOMER 
    + 4. USER
    + 5. NHỮNG NGƯỜI CÒN LẠI, SẤP , CÁC BÊN    
- BA - BUSINESS ANALYST - LÀ CÂU CHUYỆN CHÍNH CỦA CHÚNG TA
* ĐỊNH NGHĨA VỀ BA
- Là mọt gã trong team, giao tiếp với các thành viên trong dev team, và giao tiếp với bên ngoài dev team, tức là giao tiếp với khách hàng và user
- Gã giao tiếp với developer về tính năng phần mềm cần làm
- Gã giao tiếp với QC/Tester về tính năng phần mềm cần test
- Gã giao tiếp với PM về tiến bộ, dộ phức tạp của tính năng phần mềm
- Gã giao tiếp với khách hàng/user để tìm ra các tính năng phần mềm và đem về cho dev team làm 


# 1. REQ DEVELOPMENT - TÌM RA CÁC REQUIREMENTS TÍNH NĂNG CỦA PHẦN MỀM 
- đây là công đoạn, hay gồm những việc quan trọng: tìm ra tính năng 
- Trong công đoạn này gồm 4 giai đoạn con 
1. a ELICITATION (ÁP DỤNG CÁC SKILL LÀM VIỆC VỚI KHÁCH HÀNG, USER ĐỂ LẤY ĐƯỢC MONG ƯỚC CỦA HỌ VỀ PM)


2.



===============================================================================================================================================================
1A. CÓ KHOẢNG 10+  CÁC KĨ THUẬT ĐỂ LÀM VIỆC VỚI KHÁCH HÀNG 
(1): interviewing 
(2): workshop - tổ chức phiên họp nhiều user/kh 
(3): focus group - tổ chức phiên họp nhiều user/kh cùng tham gia 
(4): questionaire/survey: làm bản điều tra câu hỏi, nhu cầu số đông 
(5): observation/ethnography: qun sát khách hàng đang làm việc để hiểu luồng thông tin, luông xử lí công việ của họ > ra được các luồng màn mànhinhf sau này của app 
(6): document collection: gom, xin tất cả các tài liệu văn bản, giấy tờ, của kh 
(7): user interface analysis: xem app đối thủ có trên thị trường, xem các app có sẵn của cùng phân khúc, app cũ nếu k/h đang dùng học từ app của thiên hạ 
(8): system interface anlysis: ko nhìn app mình là 1 đơn thể biệt lập mà app mình giao tiếp với app khác !! app có kết nối qua ví, giao hàng, google api 
(9): prototyping: phác thảo nhanh các UI, các màn hình để cho khách hàng/user cảm nhận sớm, và cho feedback
(10): brain-storming: họp chung, đề xuất ý tưởng 1 cách độc lập, 

================================================================================================================================================================
TUYỆT CHIÊU / TUYỆT KĨ / BÍ KÍP RÌM REQ TỪ KHÁCH HÀNG. TỪ USER, TỪ BÁ TÁNH
[1]. APP VIẾT CHO NHỮNG AI DÙNG 
    - App cos 2 module
        + user thường
        + user quản trị/ user quản lí 
[2]. 
[3]. 
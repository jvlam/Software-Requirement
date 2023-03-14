# khi làm một app bất kì luôn luôn có 3 câu hỏi 
# 1. App viết cho ai sử dụng 
- về mặt logic, chính là màn hình login 
- 2 loại user 
    + user thường : ít quyền và chủ yếu là view, read
        + guest, visitor - không cần login mà vẫn dùng được app 
        + có account, member 
    + user quản trị : crud, tạo data cho user thường 
# 2. App có tính năng gì, ai làm được gì với app
- VERD what 
# 3. Data gì được lưu trữ và xử lý 

# NHẬP MÔN USE CASE DIAGRAM (UCD)- Sơ Đồ Tình Huống Sử Dụng App
## I Định Nghĩa:
- Là một loại sơ đồ đi kèm với nhiều loại sơ đồ khác thuộc trường phái vẽ tên là UML  (Unified Modeling Language)
    + UML là tập hợp của nhiều loại sơ đồ khác nhau trong suốt quá trình công đoạn làm phần mềm
    + mỗi loại sơ đồ gắn với một vài giai đoạn làm phần mềm (nghĩa là giai đoạn nào cũng có sơ đồ)
        - 1. Requirement
        - 2. Design
        - 3. Code
        - 4. Validation
        - 5. Deployment 
        - 6. Mainternance
- UCD là sơ đồ gắn với giai đoạn Requirement ở trên
- UCD là sơ đồ liệt kê CÁC CHỨC NĂNG/TÍNH NĂNG/TÊN MÀN HÌNH CỦA APP SẼ ĐANG LÀM CHO KHÁCH HÀNG, VÀ LIỆT KÊ CÁC USER XÀI APP ĐÓ, XÀI TÍNH NĂNG GÌ !!

## II CÁC THÀNH PHẦN TẠO NÊN UCD, CÚ PHÁP VẼ UCD 
### 1. SYSTEM BOUNDARY - biên của hệ thống - biên giới của app
- LÀ 1 HÌNH CHỮ NHẬT, TRÊN CÙNG CÓ TÊN CỦA APP SẼ LÀM 
- MỌI ACTOR (USER) PHẢI NẰM BÊN NGOÀI HÌNH CHỮ NHẬT
- MỌI TÍNH NĂNG, CHỨC NĂNG CỦA APP, PHẢI NẰM TRONG HÌNH CHỮ NHẬT 
- HÌNH CHỮ NHẬT, khoanh vùng trong và ngoài, trong nghĩa là những tính năng sẽ cung cấp cho user trải nghiệm
- Bên ngoài System Boundary sẽ là user/actor hoặc các app khác có tương tác với app mình, 
    + hoặc các thiết bị khác có tương tác với app mình
    + tương tác hiểu là: cung cấp info cho app mình, nhận info từ app mình, kích hoạt app mình, run tính năng nào đó
### 2. ACTOR (HÌNH NGƯỜI QUE) DỊCH LÀ TÁC NHÂN 
- LÀ CON NGƯỜI, LÀ USER xài app, xài các tính năng của app 
- Có 2 loại user (đã nói ở trên rồi) đó: user thường và user quyền lực/quản trị 
    + user thường có user cực kì đặc biệt: ko login vẫn xài app, xài được một số tính năng gọi là : GUEST
    + những user còn lại (thường, quản trị) đều cần login để xài đc nững tính năng đã đucowj phân quyền 
        + HỌ GỌI CHUNG LÀ MEMBER, REGISTERED USER, AUTHENTICATED 
        
    * CÁCH ĐẶT TÊN CHO ACTOR, USER: NOUN, DANH TỪ, không dùng tên riêng Lan Hồng Huệ Mơ Mận Đào làm actor
        - nếu các bạn này đều cùng 1 công việc là tạo mới đơn hàng và thu tiền, các em gọi chung là: Thu Ngân - Cashier 
    * ACTOR CÒN LÀ APP KHÁC CÓ TƯƠNG TÁC VỚI APP TA, ACTOR CÒN LÀ THIẾT BỊ KHÁC CÓ TƯƠNG TÁC VỚI APP TA
        - vd: nếu ta có login = gmail, thì gmail sẽ cung cấp info cho app ta, rõ ràng nó là 1 "user" nó có xài tính năng nào đó
    * APP giám sát an ninh, app bãi giữ xe thông minh, cần nhận info từ Camera, 
        - Camera đc xem là actor, vì có gửi info cho app          
    - NHỮNG THIẾT BỊ ĐI KÈM VỚI APP TA VIẾT, VÀ CUNG CẤP NHIỀU INFO CHO APP HOẠT ĐỘNG, NHỮNG THIẾT BỊ NÀY CŨNG LÀ HÌNH NGƯỜI que - ACTOR
        - ví dụ: Camera giám sát, Sensor (cảm biến) trong app Iot, nhưng gửi info quá đơn giản, 
        - QR, barcode, thì không cần vẽ ra cũng đc cho sơ đồ bớt rối!!
    * CÒN 1 ACTOR CỰC KÌ ĐẶC BIỆT KHÁC, ĐÓ LÀ: SYSTEM HANDLER 
    Khi app chúng ta viết, có tình huống là tự động làm 1 việc gì đó khi đến thời điểm nào đó                    
        - Ví dụ: đơn hàng đặt hàng sau 24 giờ ko thanh toán, tự bị hủy 
        - app nhắc thuốc: cứ đến 3 giờ chiều thì app nhắc người già uống thuốc                                                                                          
        - app quản lí lịch làm việc: cứ trước event quan trọng 30p, 1 ngày thì nhắc                                                       
        - app cào data: 23:59 phút tối thứ 6, lên website tgdd, cellphones, hoangha fpt shop lấy các dữ liệu điện thoại                              
            - đoạn code này thay cho admin làm việc gì đó
            - đoạn code này kích haoatj app chạy, nó được gọi là, nhân cách hóa thành 1 USER gọi là: SYSTEM HANLDER 
            - từ khóa CRON JOB  
### 3. USECASE (hình ô-val, elipse) USECASE - TÌNH HUỐNG SỬ DỤNG 
- là tên gọi của 1 chức năng, 1 tính năng, 1 user req, 1 functional req, 1 user story, 1 hoặc vài màn hình GIÚP NGƯỜI DÙNG LÀM 1 CÔNG VIỆC GÌ ĐÓ
- 1 UC LÀ 1 CHỨC NĂNG MÀ APP PHẢI GIÚP GÌ ĐÓ CHO NGƯỜI DÙNG
- 1 UC LÀ 1 XỬ LÍ, ĐÒI HỎI APP PHẢI CÓ HÀNH ĐỘNG TÍNH TOÁN, XỬ LÍ, LƯU TRỮ PHẢI TRẢ VỀ 1 KẾT QUẢ CÓ Ý NGHĨA CHO NGƯỜI XÀI
* CÁCH NHẬN DIỆN NÓ:
    + dùng động từ mô tả cái what mà user sẽ đạt được khi xài tính năng!!!
    + động từ bao hàm 2 nghĩa: lưu trữ info, xử lí info 
* QUY TẮC ĐẶT TÊN UC
    + verb - object động từ + bổ ngữ, ví dụ: Create an order, Ban a user, Update a product, Search items, Choose map, Sell item 
* COI CHỪNG NHẦM LẪN ["USE CASE"]() VÀ ["STEP"] ĐỂ HOÀN TẤT USE CASE 
    - ["USE CASE"](): khi app sẽ phải trả về 1 thứ gì đó cho user
        + Login trả về: đc xác thực, mới làm được gì đó tiếp, 
        + Create an order: trả về đơn mua hàng được tạo ra 
        + Search products: trả về danh sách sản phẩm thỏa keyword
        + Sell items: bán dc, thu dc tiền / coin từ việc bán
        + Buy items: mua đc món đồ trang bị cho tướng của mình

    - ["STEP"](): cũng có động từ chỉ hành động, nhưng app chẳng xử lí gì cả, vì nó chỉ là 1 bước góp vào việc xử lí Use Case
        + input username -> app chả làm gì
        + input password -> app chả làm gì
        2 thằng này là 2 step để hoàn tát góp phần cho UC login chạy thành công !!!
        2 thằng này ko là UC

        select destination, choose country -> app chả xử lí gì 
        vì nó là 2 step để hoàn tất tính năng UC BOOK VÉ, BOOK PHÒNG!!! 
### 4. LINK - nét nối CÓ NHỮNG CÁCH THỨC KẾT NỐI CÁC THÀNH PHẦN TRONG SƠ ĐỒ UC VÀ DÙNG LẠI 4 LOẠI NÉT NỐI DƯỚI ĐÂY
    - Association 
        + 
    - Generalization 
    - Include 
    - Extend 
    * 1. ACTOR NỐI VỚI ACTOR 
        - chỉ được sử dụng nét nối tam giác rỗng, nét nối mang ý nghĩa kế thừa, generalization 
        - con hướng tam giác rỗng về cha
        - dùng khi các actor chia sẻ chung/ dùng chúng các tính năng nào đó!!!
            + Lecturer---------------|> Member
            + Student----------------|> Member
            + Sales Manager----------|> Member
    * 2. ACTOR NỐI VỚI USE CASE 
        - chỉ đc sử dụng 1 nét nối duy nhất là ASSOCIATION, MANG Ý NGHĨA USER X XÀI TÍNH NĂNG Y 
    * 3. USE CASE NỐI VỚI USE CASE 
        - có 3 cách nối giữa 2 UC với nhau, tùy bài toán, tùy app
            + cách 1: Generalization, tam giác rỗng từ UC Con hướng về UC cha
                + mang ý nghĩa: giữa các UC có những đặc điểm chung, xử lí chung nào đó đọc đc câu A is a B 1 chiều dùng loại nét này để gom chức năng, gom menu
                + Ví Dụ: (Manage item) là UC cha
                        - Create an item là con
                        - Update an item là con
                        - Delete an item là con
                        - Search items là con
                + CÔNG THỨC CHUNG: MANAGE X LÀ CHA, CRUD X LÀ CON 
            + cách 2: Include Phụ thuộc siêu chặt chẽ, sống còn
            + cách 3: Extend Phụ thuộc lỏng lẻo, option, plugin 

----------------------------------------------------------------------------------------------------------------------------------------
# MỞ RỘNG
- UC LÀ TÍNH NĂNG, LÀ MÀN HÌNH LÀM GÌ ĐÓ CHO USER, ACTOR
    + UC LÀ FUNCTIONAL REQS, USER REQS, USER STORY  
    + GIỮA CÁC TÍNH NĂNG CÓ THỂ CÓ SỰ LIÊN KẾT NÀO ĐÓ
1. ["LIÊN KẾT THEO KIỂU GOM NHÓM, CÓ ĐIỂM TƯƠNG ĐỒNG, MỐI QUAN HỆ IS-A"]()
    + (Con) ---------------|> (Cha)
    + .... .

2. ["LIÊN KẾT PHỤ THUỘC CHẶT CHẼ"]()
- CÓ NHỮNG USE CASE (2 TRỞ LÊN) MÀ CHÚNG PHỤ THUỘC RẤT CHẶT CHẼ, TỨC LÀ THẰNG NÀY MUỐN XONG, THÌ CẦN THẰNG KIA GIÚP, THẰNG KIA CŨNG PHẢI XONG
THÌ THẰNG NÀY XONG MỚI ĐƯỢC
- tính năng đăng kí member (Sign-up) thì luôn có 1 tính năng ngầm: gửi Email(kích hoạt, hoặc thông tin account)
- nếu đăng kí thành công, đồng nghĩa với việc email đã đc gửi đi !!!
- (BASE UC) -------------<<include>>----------------> (UC phụ thuộc, included)
    Base ko thể thành công nếu thiếu bên phụ thuộc
     y chang khái niệm app mình cần thư viện, cần dependency, thiếu thư viện, ko chạy app đc <<INCLUDE>> ĐỌC TỪ GỐC MŨI TÊN
- DÙNG <<INCLUDE>> KHI CÓ NHIỀU UC XÀI CHUNG 1 USE CASE NÀO ĐÓ, HOẶC CÓ NHỮNG XỬ LÍ LẶP ĐI LẶP LẠI TRONG CÁC UC, TÁCH XỬ LÍ CHUNG NÀY RA THÀNH UC THƯ VIỆN 
    + reset, sign-up đều có 

3. ["LIÊN KẾT PHỤ THUỘC LỎNG LẺO - EXTEND, PLUGIN, OPTION"]()
- (BASE UC - UC CHÍNH) <|---------------<<extend>>---------(USE CASE EXTENSION)
-       (Search) <|---------------<<extend>>-----------(View detail)
- BASE UC có thể hoàn tất mà chẳng cần gì đến (mở rộng, plugin, option) thích thì gọi, mà không thích thì thôi 
* DÙNG EXTEND KHI NÀO: KHI MUỐN LIÊN KẾT CÁC TÍNH NĂNG CHO TIỆN SỬ DỤNG, TỪ MÀN HÌNH NÀY CHUYỂN SANG MÀN HÌNH KHÁC MÀ KHÔNG CẦN ĐI QUA MENU 
    - trong danh sách kết quả search thường có link trên từng dòng kết quả để view detail thùng rác kế bên từng dòng để thích thì xóa

---------------------------------------------------------------------------------------------------------------------------------------------------------
# TÓM LƯỢC / TỔNG LƯỢC VỀ UCD - USE CASE DIAGRAM
* UCD là sơ đồ liệt kê các tính năng, chức năng, tên màn hình, functional reqs, user story, user requirements, use case - các tình huống sử dụng app
* UCD là sơ đồ liệt kê các tính năng của app và những user (actor) xài các tính năng đó           
                                                                         
# CÓ 4 THÀNH PHẦN TẠO NÊN SƠ ĐỒ NÀY 
## 1. SYSTEM BOUNDARY - HCN, ĐI KÈM TÊN APP PHÍA TRÊN 
## 2. USE CASE - hình elipse/oval chính là 1 tính năng, 1 .., dùng verb + object để làm một điều gì đó cho user 
               - mà nếu không có nó thì user vẫn phải làm = tay 
## 3. ACTOR - con người/ user xài app, một thiết bị, app khác cung cấp với app mình đang viết 
            - 2 loại user: có login và ko login 
            - 2 loại user: user thường và user quyền lực
                       guest và có login   phải login 
## 4. LINK - NÉT NỐI GIỮA 3 THÀNH PHẦN TRÊN
### * actor nối với actor: generalization 
### * actor nối với use case: association
### * use case nối với use case:
        - UC Cha <|---------- UC Con: generalization
        - (Base UC) ---------<<Include>>----------> (Included UC, UC phụ thuộc, thư viện, đọc từ base, gốc mũi tên, tao cần mày ở bên kia)
        - (Base UC) <-------------<<extend>>-------- (extend, extension, plugin, option) đọc từ

-----------------------------------------------------------------------------------------------------------------------------------------------------------

# UC là hình elipse, oval, diễn tả một chức năng, 1 tính năng, 1 tên màn hình, 1 functional req, 1 user req, 1 user story 
  giúp user xử lí 1 công việc gì đó, giúp user làm đc 1 điều gì cho công việc của user

- Ví dụ:
    (Create an order) giúp cho thu-ngân/cashier ghi nhận được giao dịch mua hàng 
    (Ban a user) giúp admin/mod cấm 1 user nào đó hay phá đám / spam
    (login) giúp 1 user nào đó có account sãn sàng đăng nhập để làm đc những việc mà user thường không làm đc
    (update) giúp sales 

- UC đủ để dev team, user, người đặt hàng làm app hiểu cơ bản về tính năng mà họ sẽ trải nghiệm, nhưng nó lại khá chung chung, 
thiếu chi tiết cho phần hiện thực tính năng ở giai đoạn code/design 

Ví dụ : Guest thì register/sign-up
        Member thì login 
2 tính năng trên kho khó hiểu, dân thường cx hiểu đc, dân dev hiểu đc luô nhưng dân dev lại bối rối 
Bối rối không phải vì kông code đc, mà là vì nhiều phương án để code!!!
Ví dụ: sign-up có các cách thức sau :
    - gõ vào số di động, gửi OTP -> nhập đúng OTP tương đương tạo mới + đăng nhập 
    - sign-up = cách dùng Gmail, FB đang active         
    - sign-up = cách dùng email address nhưng pass riêng!!
    - sign-up = cách dùng username, pass riêng                                                                                                            


- PHIẾU NÀY ĐƯỢC GỌI LÀ: USE CASE DESCRIPTION - ĐẶC TẢ USE CASE 

UCD PETSTORE
- (Login) -------------------- 1 UC Desc
- (View profile)-------------- 1 UC Desc
- (Update profile)------------ 1 UC Desc
- (Create pet)
- (Create service)
- (Create item)

# CÂU SỐ 3: HÃY VIẾT 1 UC DESC PHIẾU MÔ TẢ UC VIẾT THẾ NÀO ??
- VIẾT TỰ DO DÙNG NOTEPAD
- VIẾT THEO 1 FORMAT CHO TRƯỚC ĐỂ ĐẢM BẢO CHUYÊN NGHIỆP, KO THIẾU INFO!!! 
- MỘT UC DESC CÓ NHỮNG THÀNH PHẦN CƠ BẢN SAU, MÔ TẢ CHI TIẾT 1 UC GỒM NHỮNG MỤC SUA
1. MÃ số UC:______________
2. Tên UC: _____________
3. Ai tạo ra UC này: ____________ tên gã BA
4. Ngày giờ tạo ra UC này: ___________ sau khi đi lấy y/c về, bắt đầu vẽ
5. Mô tả vắn tắt về UC: ____________
6. KHi nào UC này đc chạy, tính năng được chạy (trigger): ___________
7. Để chạy UC này, cần có những điều kiện tiên quyết nào, data nào (pre-conditions):__________
8. Sau khi UC chạy xong, tính năng chạy xong, trạng thái của app ra sao, db thế nào (post-conditions): ___________
9. Kịch bản chạy tính năng này, các xử lí của tính năng này, các step của UC này: 
    Main flow:
10. Kịch bản thay thế dự phòng: __________
    Alternative flow:
11. Kịch bản thảm họa, khi chạy UC bị crash, ngoại lệ gì, nói luôn ở đây 
    Exception flow
12. Business rules: quy tắc xử lí của user/actor trong công việc của họ những gài về data họ muốn app làm!!!




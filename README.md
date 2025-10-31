# Khien_dieu_hoa_thong_minh_phan_hoi_2_chieu_Homekit_Home_Assistant_Hass
3.HƯỚNG DẪN SỬ DỤNG KHIỂN ĐIỀU HÒA THÔNG MINH APPLE HOMEKIT, WEB
HƯỚNG DẪN SỬ DỤNG
THIẾT BỊ ĐIỀU KHIỂN ĐIỀU HÒA THÔNG MINH 
PHẢN HỒI 2 CHIỀU LÊN TRỰC TIẾP HOMEKIT/HOME ASSISTANT

I.	Chức năng chính
1.	Khiển điều hoà tích hợp được cả Apple Homekit , Home Assistant. Điều khiển qua Trình duyệt Web trên PC và Smart Phone, điều khiển phản hồi 2 chiều. Đọc lệnh khiển để tự nhận diện loại điều hoà.
2.	Phản hồi tín hiệu hồng ngoại 2 chiều: Khi điều khiển phổ thông phát lệnh bật, tắt, làm lạnh, sưởi ấm, tốc độ gió tới điều hòa thì trên Apple Homekit đồng thời cập nhập trạng thái tương ứng của thiết bị.
3.	Nếu cần điều khiển thiết bị bên ngoài mạng nội bộ cần dùng các thiết bị làm máy chủ như HomePod, HomePod mini, Apple TV hoặc iPad để kết nối từ xa. Hoặc thông qua máy chủ Home Asisstant
4.	Hỗ trợ điều khiển công tắc, chế độ, nhiệt độ, tốc độ gió, góc quét của điều hòa
5.	Hỗ trợ hàng chục giao thức điều khiển từ xa điều hòa không khí, điều khiển hồng ngoại 
II.	Kết nối WiFi
1.	 Sau khi cắm nguồn, thiết bị nếu không có kết nối mạng/mất mạng thì đèn LED xanh nháy liên tục, đồng thời tạo ra điểm truy cập có tên ESP_CONFIG_XXXXXX, với XXXXXX  là địa chỉ MAC của thiết bị cần ghi lại tránh quên và sử dụng sau đó để truy cập vào thiết bị sau khi kết nối wifi thành công.
2.	Dùng điện thoại, máy tính...kết nối điểm truy cập sau đó nó sẽ tự động nhảy vào giao diện thiết lập wifi, nếu không tự động vào trang cài đặt có thể truy cập thủ công, nhập 192.168.4.1
<img width="170" height="270" alt="image" src="https://github.com/user-attachments/assets/c1ea24eb-2ffc-4b1d-8d79-15f3f4325f38" />
<img width="208" height="270" alt="image" src="https://github.com/user-attachments/assets/ceadafc6-ea2e-4157-9f51-3a72ced622f8" />
          
-	Quét WiFi, điền tên và mật khẩu WiFi, sau đó nhấp vào Gửi cấu hình. Sau khi kết nối thành công, sẽ tự động thoát khỏi chế độ cấu hình mạng và tắt điểm phát sóng AP.
-	Chỉ báo trạng thái WiFi IO2 (D2): Là đèn LED màu xanh gần ăng-ten trên chip, nhấp nháy liên tục khi không kết nối Internet và tắt khi kết nối Internet.
III.	Truy cập vào thiết bị sau khi kết nối wifi thành công
-	Sau khi thiết bị truy cập wifi thành công thì tiến hành truy cập thiết bị thông qua địa chỉ có định dạng: ESP-XXXXXX.local . Tiến hành truy cập thành công có thể bỏ qua bước IV
-	Ví dụ như thiết bị phía trên có cấu hình ESP_CONFIG_0C2C35 => địa chỉ truy cập như sau: ESP-0C2C35.local
IV.	  Tìm địa chỉ IP và truy cập thiết bị khi quên tên thiết bị hoặc vấn đề khác
Nếu không thể vào trực tiếp qua đường dẫn định dạng ESP-XXXXXX.local thì có thế tìm IP để truy cập, nhưng địa chỉ IP là không cố định nên mỗi lần vào là có thể 1 IP khác nhau, tối ưu nhất vẫn là dùng định dạng ESP-XXXXXX.local là cố định với mỗi thiết bị.
Sau khi thiết bị đã nhận Wifi thì tiến hành xác định địa chỉ IP mạng của thiết bị dựa vào địa chỉ MAC:
-	Thiết bị tìm IP cần có kết nối Wifi với thiết bị khiển điều hòa thông minh.
-	Ví dụ thiết bị:
•	Có điểm truy cập: ESP_CONFIG_0C2C35
•	Địa chỉ MAC: 0C2C35
•	Địa chỉ IP: 192.168.0.31
-	Các cách cho từng thiết bị khác nhau:
1.	Trên máy tính chạy Window dùng ứng dựng có “Advanced IP Scanner”. Nhấn “Quét” tìm IP thiết bị có địa chỉ MAC cần tìm:
<img width="358" height="393" alt="image" src="https://github.com/user-attachments/assets/0dee2cdb-0893-4092-b0a2-e46f03c880fa" />
 
2.	Trên Iphone dùng phần mềm “ScanNet” để tìm địa chỉ IP:
Tìm ứng dụng trong Apple Store và cài đặt. Sau khi cài đặt bật ứng dựng và nhấn “Scan”tìm IP  thiết bị có tên giống như địa chỉ MAC:
<img width="285" height="265" alt="image" src="https://github.com/user-attachments/assets/bd2f246e-226a-4a7c-a1a3-9516da43bee3" />
<img width="212" height="269" alt="image" src="https://github.com/user-attachments/assets/9951cead-cc95-4bfc-b590-2fdf82700efa" />
 	 

3.	Trên điện thoại Android dùng phần mềm “Network Scanner” để tìm địa chỉ IP:
Tìm ứng dụng trong “CH Play” và cài đặt. Sau khi cài đặt bật ứng dựng và nhấn “Scan”tìm IP  thiết bị có tên giống như địa chỉ MAC:
<img width="246" height="241" alt="image" src="https://github.com/user-attachments/assets/3c6e3c47-7d43-495f-83c2-3075577af6dc" />
<img width="181" height="240" alt="image" src="https://github.com/user-attachments/assets/7c3f48f0-01b4-415d-abf7-f3c19f4a6407" />
       
4.	Tìm trong bộ phát Wifi mà thiết bị đã kết nối:
<img width="374" height="266" alt="image" src="https://github.com/user-attachments/assets/37ca5a53-5d12-409e-9502-cf0f7cd828f8" />
 












V.	Thiết lập cài đặt thiết bị
-	Sau khi truy cập địa chỉ IP thiết bị, tiến hành cài đặt nhận diện điều hòa cần sử dụng:
<img width="226" height="421" alt="image" src="https://github.com/user-attachments/assets/fd162e1d-baa6-48a8-8141-b3a0482c06bb" />
<img width="238" height="417" alt="image" src="https://github.com/user-attachments/assets/d1646b8c-7580-4b38-838e-1316b269929d" />
          

-	Thiết lập cấu hình nhận diện điều hòa có 2 cách:
Cách 1: Chọn theo tên điều hòa trên dòng “Loại điều hòa”
Cách 2: Nhấn vào “Hỗ trợ nhận biết” và chọn “OK” sau đó dùng khiển điều hòa chỉ vào mắt thu của thiết bị thông minh nhấn “On/Off” bất kì trên điều khiển cầm tay của điều hòa, sau đó tên thiết bị trên loại điều hòa sẽ tự động thay đổi là xong.
-	Nếu thiết bị đã được nhận diện xong thì sẽ nhấp nháy đèn LED xanh khi có tín hiệu phát ra từ điều khiển cầm tay.
-	Các thiết lập trong Tab GPIO và Info không nên thay đổi, tránh ảnh hưởng đến sự hoạt động bình thường của thiết bị
VI.	Thêm thiết bị vào HomeKit và sử dụng
1.	Tải và cài đặt ứng dụng Apple Homekit (Nhà) từ kho ứng dụng Apple Store, 
<img width="239" height="336" alt="image" src="https://github.com/user-attachments/assets/46ced525-8a3a-4498-bc26-c7a8ee7e3949" />
<img width="179" height="338" alt="image" src="https://github.com/user-attachments/assets/c3b8d3e2-47e5-4bf8-bc7c-fd7d1cc86205" />
        
2.	Sau khi thiết bị cài đặt ứng dụng kết nối đúng mạng với thiết bị điều khiển thì mở ứng dụng nên. Nhấn dấu cộng góc phải màn hình sau đó chọn “Thêm phụ kiện”
<img width="203" height="163" alt="image" src="https://github.com/user-attachments/assets/d1990df1-4161-4a97-bdba-0ad7ce9d79d1" />
<img width="238" height="164" alt="image" src="https://github.com/user-attachments/assets/078b3566-3885-421c-927f-026740117262" />
<img width="117" height="164" alt="image" src="https://github.com/user-attachments/assets/5b574052-bc87-467d-8172-074ec35bad71" />
          
-	Dùng điện thoại Iphone hoặc Ipad ấn “ Tùy chọn khác…” để nhập mã thiết bị: 
111-11-111 và làm theo các bước của phần mềm gợi ý. Chọn “Vẫn thêm” khi có yêu cầu         
<img width="105" height="210" alt="image" src="https://github.com/user-attachments/assets/9d49aa46-29f3-45dc-bbee-c744ab63b21b" />
<img width="110" height="210" alt="image" src="https://github.com/user-attachments/assets/2e61b7d4-5eb8-48e6-98ab-bef813ef99a2" />
<img width="101" height="210" alt="image" src="https://github.com/user-attachments/assets/4bbbe4e4-9c8a-49eb-96b0-e102a312bd85" />
<img width="105" height="210" alt="image" src="https://github.com/user-attachments/assets/329e9e21-0b23-41b1-a507-9f602d1fc3f2" />
<img width="120" height="210" alt="image" src="https://github.com/user-attachments/assets/53d6771b-c044-4367-875f-326cfe59932d" />
             


VII.	Thêm thiết bị vào Home Asisstant và sử dụng
Trong ứng dụng để thêm thiết bị Homekit vào chúng ta làm theo các bước sau:
<img width="127" height="258" alt="image" src="https://github.com/user-attachments/assets/7cc7e50d-99f5-4e32-904c-448fae8df601" />
<img width="127" height="257" alt="image" src="https://github.com/user-attachments/assets/4055def7-3676-4727-80f8-a8d26362d759" />
<img width="141" height="259" alt="image" src="https://github.com/user-attachments/assets/1b85c6c2-a825-4e5f-b82b-94155457ca35" />
<img width="170" height="257" alt="image" src="https://github.com/user-attachments/assets/12645220-3a6a-4e73-963a-eb8212b7daba" />
          
Sau đó thêm nhập mã thiết bị: 111-11-111 và làm theo các bước của phần mềm gợi ý.
VIII.	Điều khiển thiết bị trên trình duyệt Web và thêm ra màn hình chính để sử dụng.
1.	Truy cập địa chỉ IP thiết bị và thao tác nhấn nút “ Send IR” sau khi đã thiết lập chế độ mong muốn trong “Điều khiển AC” để phát lệnh điều khiển cho điều hòa.
<img width="241" height="448" alt="image" src="https://github.com/user-attachments/assets/64dd34d5-54ab-4657-8157-d55fc1852a92" />
 
2.	Thêm trình duyệt Web ra màn hình chính theo trình tự sau:
<img width="130" height="260" alt="image" src="https://github.com/user-attachments/assets/3de7413b-b28f-461a-8303-00b1e65bbfd3" />
<img width="130" height="248" alt="image" src="https://github.com/user-attachments/assets/baa3878b-d9bf-48c6-8075-0f9e05292f47" />
<img width="131" height="247" alt="image" src="https://github.com/user-attachments/assets/d29d6ae2-4b11-4f20-801d-3d6de358cc5a" />
<img width="122" height="247" alt="image" src="https://github.com/user-attachments/assets/f3d011e6-25b5-4fea-ae65-c300ddcb41c7" />
                
IX.	Chức năng nút ấn và các chú ý
1. Trên thiết bị có 1 nút ấn nhỏ: Nhấn giữ nút Setup khi LED xanh nhấp nháy liên tục thì nhả tay để thiết bị xóa bỏ thiết lập Homekit, thiết lập lại Homekit trên thiết bị mong muốn khác.
2. Khi thiết bị không hỗ trợ nhận biết loại điều hòa thì mã điều hòa không được hỗ trợ và cần chọn mã điều hòa tương ứng xem có điều khiển được điều hòa không, lúc này thiết bị không thể phản hồi tín hiệu khiển cầm tay
X.	Hỗ trợ sản phẩm
- Hiện tại các phiên bản Khiển điều hoà thông minh đầy đủ các option để các ace có nhu cầu dễ dàng lựa chọn nhé: 
1. Loại cắm dây Type C
Kích thước nhỏ gọn: 5.25x2.35cm
<img width="159" height="215" alt="image" src="https://github.com/user-attachments/assets/4fde96ae-06c3-49fc-9f75-9110f2f0e5d0" />

3. Loại cắm dây cáp dẫn hướng USB dễ dàng định hướng bất kỳ 
Kích thước nhỏ gọn: 5.25x2.35cm	 
<img width="162" height="213" alt="image" src="https://github.com/user-attachments/assets/0e95fe11-2ccf-4ca0-88b6-bac39ef66f50" />


- Thông tin tư vấn, hỗ trợ trực tiếp: 
1. Nhóm zalo chứa các hướng dẫn và tài liệu cài đặt, sử dụng thiết bị: 

Cách 1: Link https://zalo.me/g/wwvddo214 
<img width="284" height="261" alt="image" src="https://github.com/user-attachments/assets/65625885-0534-4d49-94bd-62253e77461d" />









Cách 2: Quét mã để truy cập nhóm
	 

2. SĐT/Zalo/Wechat: 0335361383 
- Thông tin sản phẩm: 
1. Cảm biến hiện diện: https://vn.shp.ee/TpTgUMY 
2. Khiển điều hoà thông minh: https://vn.shp.ee/T288wVs 
- Link HDSD: 
1. Hướng dẫn thêm thiết bị cảm biến hiện diện vào Apple Homekit: https://www.facebook.com/share/v/VAV1hzeT6LBdF4XB/?mibextid=WC7FNe 
2.Hướng dẫn thêm thiết bị cảm biến hiện diện vào Home Assistant (HASS): https://www.facebook.com/share/v/xWU88qsVTGcKDamD/?mibextid=WC7FNe 
3. Hướng dẫn cài đặt khiển điều hoà thông minh vào trực tiếp Homekit/Hass: https://www.youtube.com/watch?v=59d_Zl6w95A 
4. Tìm chúng tối trên Facebook: https://www.facebook.com/x.smart.link?mibextid=LQQJ4d
#XSmartLink #GiaiPhapThongMinh #HVAC_XSmartLink #Shoppe_XSmartShop #Thiet_Bi_Nha_Thong_Minh #XSmartShop #CamBienHienDien #CBHD #LD2410 #Homekit #Nhietdo #Doam #Tasmota #Homekit #Hass #HomeAssistant #XSmartHome


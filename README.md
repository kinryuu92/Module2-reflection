# Module2-reflection-ngày 26/1
***
- Mảng là biến đặc biệt, chứa nhiều giá trị tại một thời điểm. có ba loại mảng : 
  - Mảng 1 chiều với chỉ số
  - Mảng 1 chiều với chỉ số là từ khóa
  - Mảng đa chiều chứa nhiều mảng
  
- Các cách sắp xếp mảng: 
  - soft() - sắp xếp mảng tăng dần
  - rsoft() - sắp xếp mảng giảm dần
  - asoft() - xếp mảng tăng dần theo từ khóa
  - arsoft() - xếp mảng tăng dần theo giá trị
  - ksoft () - xếp mảng giảm dần theo từ khóa
  - krsoft() - xếp mảng giảm dần theo giá trị
***
# reflection Lệnh require - require_once - include - include_once
- Cả 4 lệnh đều dùng để import 1 file khác vào file hiện tại, mục đích giúp cho file khác có thể sử dụng các thư viện file hiện tại
- Sự khác biệt giữa 2 là require và require_one nếu chương trình bị lỗi thì lập tức sẽ dừng lại và ra thông báo lỗi. Còn nếu sử dụng include thì sẽ ra 1 lời cảnh bảo nhưng vẫn chạy đến chương trình
- Khác biệt giữa require và require_one là require_one chỉ import đúng 1 lần . Nếu dùng lệnh này ở 1 file 2 lần thì lần thứ 2 nó sẽ không thực thi nữa.
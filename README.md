
# Module2-reflection-ngày 29/1
***
- Vòng đời của một đối tượng : 
   + Khởi tạo đối tượng: __construct() --> sử dụng đối tương --> Hủy đối tương __destruct()
   
VD:
  function __construct(){     
     echo 'Calling constructor';<br/>
  }   
 
  function some_method(){     
      echo 'Calling a method';<br/>  
  }  
 
  function __destruct()    {     
       echo 'Calling destructor';<br/>   
  }
 }
 $myObject = new MyClass();<br/>
 $myObject->some_method();
   
   
- Kế thừa (Inheritance) là cơ chế cho phép một lớp con sử dụng lại các đặc điểm và hành vi của lớp cha
- Một số dạng kế thừa : 
   + Single: Một lớp kế thừa chỉ 1 lớp cha
   + Multilevel: Một lớp kế thừa tù lớp cha, lớp cha lại kế thừa lớp khác trên nó
   + Hierarchical: 1 lớp cha có nhiều lớp con với level khác nhau.
   + Multippe: Đa kế thừa -> 1 lớp con kế nhiều lớp cha (Trong JAVA không cho phép đa kế thừa )
   
- Cú pháp: 
   + class SubClass extends SuperClass{};
   trong đó: - từ khóa extends được sử dụng để kế thừa 1 lớp.
             - SubClass là tên lớp con.
             - SuperClass là tên lớp cha.
             
 - Ghi đè phương thức(Method overriding) cho phép lớp con định nghĩa lại phương thức đã định nghĩa trước đó  của lớp cha.
 
 - Từ khóa parent sử dụng trong một lớp con truy xuất các thuộc tính và phương thức của lớp cha.
 
 - Từ khóa Final hạn chế tối đa việc ghi đè, ngăn chặn kế thừa từ một lớp và việc ghi đè phương thức


# Module2-reflection-ngày 28/1
***
- JSON là đọc dữ liệu từ máy chủ Web và hiển thị dữ liệu trong một trang web
- Chuyển đổi đối tượng PHP thành JSON ta dùng hàm json_encode()
VD: 
<?php
$myObj->name = "tu";
$myObj->age = 30;
$myObj->city = "Ha Noi";
$myJSON = json_encode($myObj);
echo $myJSON;
?>

- Namespace là một hình thức đóng gói các hạng mục liên quan với nhau, nhóm các 
lớp, các hàm, các hàng, interface có liên quan đến nhau vào cùng một nơi.
- Cú pháp khai báo : namespace Name;
- Khi 1 class được định danh bằng 1 namespace thì sẽ có cú pháp sau:
new tenNamespace\tenClass();
VD: 
<?php
namespace my\name;

class MyClass {}
function myfunction() {}
const MYCONST = 1;
$a = new MyClass;
$c = new \my\name\MyClass;
$a = strlen('hi');
$d = namespace\MYCONST;
$d = __NAMESPACE__ . '\MYCONST';
echo constant($d);
?>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module2-reflection-ngày 27/1
***
- OOP mô phỏng đối tượng thực vào trong thế giới lập trình
- Khai báo một lớp bằng từ khóa class và khởi tại đối tượng bằng từ new
- Truy xuất đến thành phần đối tượng qua biến trỏ đến đối tượng, sử dung dấu (->) để truy xuất tới
- Access modifier là từ khóa dùng để quy định mức độ truy cập đến lớp và các thành phần của lớp. Có 3 mức truy cập: 
  - public: có  thể truy cập bất cứ đâu
  - private: Các phương thức và thuộc tính chỉ có thể truy cập cùng 1 lớp
  - protected: Các phương thức và thuộc tính được phép truy xuất cùng 1 lớp và ở lớp con kế thừa.
- Getter và Setter truy cập trực tiếp vào trường dữ liệu
- Phương thức khởi tao constructor là phương thức giúp khởi tạo các đối t

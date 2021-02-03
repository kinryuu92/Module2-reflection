# Module2-reflection-ngày 3/2
***
- Cấu trúc dữ liệu là cách lưu trữ, tổ chức dữ liệu có thứ tự, có hệ thống dữ liệu để dữ liệu có thể sử dụng một cách hiệu quả.
- Đặc điểm  của cấu trúc dữ liệu là: 
   + Chính xác
   + Độ phức tạp về thời gian :  thời gian chạy hay thời gian thực thi phải nhở nhất có thể
   + Độ phức tạp về bộ nhớ : Sử dụng bộ nhớ của mỗi phép tính dữ liệu nên là nhỏ nhất có thể
 - Cấu trúc dữ liệu ArrayList:
   + Là một cấu trúc dữ liệu danh sách đặc trưng, bên trong ArrayList sử dụng mảng để lưu trữ dữ liệu.
   + Thao tác với ArrayList là chậm vì nó dùng nội bộ mảng. Nếu bất kỳ phần tử nào được xóa khỏi mảng , tất cả các bit được chuyển trong bộ nhớ
   + Tốt hơn trong việc lưu trữ và truy cập dữ liệu nhờ việc truy xuất nhanh đến các phần tử, nhờ có  cơ chế truy xuất ngẫu nhiên của 1 mảng.
 - LinkedList :
   + Là một cấu trúc dữ liệu danh sách, các phần tử liên kết qua các tham chiếu tuyến tính giữa các phần tử liên tiếp nhau.
   + So với ArrayList thì thao tác của Linked nhanh hơn bởi vì nó sử dụng danh sách liên kết, do đó không cần chuyển đổi bit nào.
   + Vì thao tác dữ liệu nhanh nên các thao tác thêm sửa xóa phần tử trong LinkedList lại rất hiệu quả, bởi vì chỉ cần thay đổi tham chiếu phần tử
   
   
# Module2-reflection-ngày 2/2
***

- Clean code:
  +  Giúp công việc cộng tác nhóm, dễ hiểu code, đơn giản dễ đọc.
  +  Dễ thay đổi, bảo trì, cải tiến.
  +  Đáp ứng được tính logic
- Các cách thực hành clean code
  + Đặt các tên lớp, phương thức và biến thích hợp. Chúng phải đơn giản và có ý nghĩa và đáp ứng được ba mục đích: nó làm gì, tại sao nó tồn tại và cách nó được sử dụng.
  + Nhiều LTV thường hay viết những đoạn code quá phức tạp. Họ giao quá  nhiều trách nhiệm trong một lớp, điều này làm nó phức tạp khó duy trì vì vậy chỉ giao nhiệm vụ duy nhất cho một class
  + Commen code rất quan trong, giúp chúng ta tiết kiệm được rất nhiều thời gian.
  + Review code: 
    +  1 hàm không nên quá 30 dòng.
    +  Lớp không lên vượt quá 500 dòng
    + 1 dòng không nên dài quá 80 kí tự
    + 1 dòng chỉ chứa 1 biến
    + 1 hàm không vượt quá 5 tham số
 
- Refactoring code
  + Giúp code dễ đọc, dễ tìm hiểu, dễ tiếp cận hơn từ đó nó sẽ giúp chúng ta dễ bảo trì, mở rộng hệ thống.
- SOLID là gif?
  + Là viết của 5 chữ cái đầu tiên trong 5 nguyên tắc thiết kế hướng đối tượng. Giúp cho LTV viết ra những đoạn code dễ đọc, dễ hiểu.
  + 5 nguyên tắc bao gồm : 
    +  Single responsibility priciple: Mỗi lớp chỉ nên chịu trách nhiệm về một nhiệm vụ cụ thể nào đó. Nếu có quá nhiều chức năng sẽ trở lên khó đọc.
    +  Open/Closed principle : Không được sửa đổi một Class có sẵn, nhưng có thể mở rộng bằng kế  thừa. Theo nghuyên lý này, nếu muốn thêm chức năng cho chương trình, chúng ta nên viết class mới mở rộng class cũ ( bằng cách kế thừa hoặc sở hữu class cũ ).
    + Liskov substitution principle: Các đối tượng (instance) kiểu class con có thể thay thế các đối tượng kiểu class cha mà không gây ra lỗi.
    + Interface segregation principle : Thay vì dùng 1 interface lớn, ta nên tách thành nhiều interface nhỏ, với nhiều mục đích cụ thể.
    + Dependency inversion principle: 
          + Các module cấp cao không nên phụ thuộc vào các modules cấp thấp. Cả 2 nên phụ thuộc vào abstraction.
          + Interface (abstraction) không nên phụ thuộc vào chi tiết, mà ngược lại (Các class giao tiếp với nhau thông qua interface (abstraction), không phải thông qua implementation.)

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module2-reflection-ngày 1/2
***
<h3> Abstrack Class là gì: </h3>
   -  Lớp trừu tượng được xem như 1 class cha cha tất cả các class nó cùng bản chất, và phải dùng từ khóa extends<br>
   -  Không cho phép có các  tham số chỉ khai báo các thuộc tính và phương thức bình thường.<br>
   -  Các phương thức định nghĩa abstract trong abstract class chỉ khai báo tên hàm và không viết nội dung hàm đó. Nội dung sẽ đươc viết trong class kế thừa khi override lại phương thức đó<br>
     Ví dụ <br>
    <?php <br>
      abstract class Animal{<br>
      public $name;<br>
      abstract function run();<br>
   }<br>
      class Dog extends Animal{<br>
   } <br>
      public function run(){<br>
      echo "Con chó chạy nhanh";<br>
    }<br>
<h3> Interface là gì : </h3>
    -  Không phải là một lớp. Nó được mô tả như một bản thiết kế cho các class có chung cách thức hoạt động. <br>
    -  Không phải một lớp lên nó không định nghĩa thuộc tính và khởi taọ đối tượng mà chỉ khai báo phương thức <br>
    -  Các phương thức chỉ khai báo tên hàm và không viết nội dung hàm trong đó.<br>
    -  Không có khái niệm phạm vi phương thức, tất cả là public<br>
    -  Lớp con kế thừa interface sẽ phải ghi đè tất cả phương thức trên đó<br>
    -  Có thể kế thừa nhiều interface khác nhau bằng từ khóa implements.<br>
 ví dụ:<br>
      <?php<br>
      interface Move <br>
   {<br>
       function run();<br>
   }<br>
      class Dog implements Move<br>
   {<br>
       public function run () <br>
        echo "Con chó chạy nhanh";<br>
    }<br>

<h3> Khi nào dùng interface và khi nào dùng abstract Class. </h3><br>
Nhìn chung cả 2 đều được coi như là một bản thiết kế cho các class con kế thừa nó<br>
     Abstract class là bản thiết kế cho class: <br>
       -  Về bản chất abstract class là một bản class khai báo thêm các thuộc tính và phương thức khác không phải trừu tượng.
         nó được xem như bản thiết kế cho class vì những class extends lại từ nó ngoài override lại các phương thức trừu tượng 
         của nó thì có thể sử dụng nó.<br>
       -  Abstract thường được sử dụng trong trường hợp class kế thừa từ nó cùng bản chất<br>
     Interface là "bản thiết kế" cho Method:<br>
       -  Vì những class implements đều ghi đều phải override lại phương thức của nó<br>
       -  Interface thường được sử dụng trong trường hợp các kế  thừa không có cùng bản chất như nhau

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Module2-reflection-ngày 29/1
***
- Vòng đời của một đối tượng : 
   + Khởi tạo đối tượng: __construct() --> sử dụng đối tương --> Hủy đối tương __destruct()
   
VD:
  function __construct(){     
     echo 'Calling constructor';<br/>
  }<br/>
  function some_method(){     
      echo 'Calling a method';<br/>  
  }  
  function __destruct()    {     
       echo 'Calling destructor';<br/>   
  }<br/>
 }<br/>
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

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Module2-reflection-ngày 28/1
***
- JSON là đọc dữ liệu từ máy chủ Web và hiển thị dữ liệu trong một trang web
- Chuyển đổi đối tượng PHP thành JSON ta dùng hàm json_encode(). <br/>
VD: 
<?php
$myObj->name = "tu";<br/>
$myObj->age = 30;<br/>
$myObj->city = "Ha Noi";<br/>
$myJSON = json_encode($myObj);<br/>
echo $myJSON;<br/>
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

## Tim hiểu về PHP
---
  Thực hiện: **Phạm Văn Đạt**

  Cập nhập lần cuối: *26/2/2017*

# Mục lục 
[1. Giới thiệu về PHP](#1)        
[2. Nhúng PHP vào trang HTML](#2)   
[3. Biến và chú thích](#3)   
[4. Cấu hình Web Server](#4)   
[5. Hàm phpinfo()](#5)                
[6. Định dạng code (indentation)](#6)     
[7. Sử dụng echo, print](#7)      
[8. echo_print mã html](#8)                 
[9. Biểu thức nối chuỗi(concatenation)](#9)      
[10. Nhúng PHP vào trang HTML](#10)          
[11. Biểu thức điều kiện if else](#11)           
[12. Biểu thức điều kiện if else if else](#12)          
[13. Biểu thức gán](#13)        
[14. Biểu thức toán học](#14)                                      
[15. Toán tử tăng và gảm(increment and decrement operator)](#15)       
[16. Biểu thức so sánh](#16)             
[17. Biểu thức quan hệ(logic)](#17)                     
[18. Hàm die và exit](#18)                
[19. Vòng lặp While](#19)                   
[20. Vòng lặp for](#20)                
[21. Break và continue](#21)                   
[22. Cấu trúc rẽ nhánh Switch](#22)                    
[23. Expression matching](#23)                    
[24. Hàm(fuction)](#24)                    
[25. Hàm với tham số](#25)               
[26. Hàm với giá trị trả về](#26)               
[27. Biến toàn cục và biến cục bộ](#27)            

# Nội dung.
<a name="1"></a>
##1. Giới thiệu về PHP
- **PHP** (Hypertext Preprocessor) là một ngôn ngữ lập trình kịch bản hay một loại mã lệnh chủ yếu được dùng để phát triển các ứng dụng viết cho máy chủ(server), mã nguồn mở, dùng cho mục đích tổng quát. Nó rất thích hợp với web và có thể dễ dàng nhúng vào trang HTML. Do được tối ưu hóa cho các ứng dụng web, tốc độ nhanh, nhỏ gọn, cú pháp giống C và Java, dễ học và thời gian xây dựng sản phẩm tương đối ngắn hơn so với các ngôn ngữ khác nên PHP.
- Để tạo một trang Web động thì ta cần sử dụng ngôn ngữ PHP và hệ quản trị cơ sở dữ liệu (ví dụ như SQL) 
- Để có thể thử cá đoạn code về web của chúng ta môt cách giễ dành thì chúng ta không thể nào mà đẩy chũng lên website để thử vì nó khá tốn công và tốn thời gian. Vì thế chũng ta nên tạo 1 web server ảo trên chính máy của chũng ta để thử và khi đã ổn định rồi thì chũng ta mới đẩy lên.
- Có hai loại web server ảo phổ biến là **wampp** và **xampp** chũng ta hãy tải 1 trong hai về để cài đặt và sử dụng.
- Sau khi cài đặt song chũng ta hay truy cập vào rang web **localhost**
<img src="http://imageshack.com/a/img921/138/FNV29t.png">
- Tạo một trang PHP cow bản:
 + Tạo một file để viết PHP với đường dẫn là `Local Disk(C:)\wamp\www` và có đuôi là `.php`
 + Viết một đoạn với thẻ đóng mở:
 <img src="http://imageshack.com/a/img922/6791/HBVXgb.png">
 + Sau đó trúng ta ra trang web **localhost** chũng ta gõ thêm vào là *localhost/ten_file.php*
 <img src="http://imageshack.com/a/img923/5499/N0kPkq.png">
 <img src="http://imageshack.com/a/img922/855/6XwSeW.png">

<a name="2"></a>
##2. Nhúng PHP vào trang HTML
- File được lưu phải có đuôi là `.php` thì mới có thể nhúng PHP vào trang HTML, nếu không để đuôi đó thì nó xẽ bỏ qua luôn không được đọc đoạn PHP đó.
- **echo**: là hàm để in ra một chuỗi dạng text, thẻ HTML. Nội dung cần hiển thị có thể nằm trong dấu nháy đợn hoặc nháy kép.
- **print**: cũng tương tự như hàm **echo**, có thể in ra thêm các định dạng.

<a name="3"></a>
##3. Biến và chú thích
- Cài Web server. Sau đó bật lên và lên trình duyệt truy cập vào trang `localhost`.
- Tạo một thư mục trong thư mục `www`.
- Commen: Không có hiệu lục gì khi viết code chỉ để giải thích.
   + Dùng dấu `\\` thì dòng dduocj đánh dấu đó sẽ là comments
   + Dùng dấu `\* nội dung *\` thì phàn nội dung ở trong sẽ là comments
   + Dùng dấu `#` thì dòng đó sẽ là commen.
- Kết thúc mỗi câu lệnh là dấu `;`
- Câu lệnh **echo** xuất ra màn hình.
- Dấu **$** là phần tử bắt buộc phải có khi khai báo biến.
- Biến như là một cái hộp để đựng những giá trị cần thiết. Khi khai báo biến thì nó được cấp cho một vùng nhớ và nó có thể lưu trữ hay gán giá trị vào và có ý nghĩa trong xuất chương trình. Biến này có thể thay đổi giá trị trong quá trình sử dụng và nó có tác dụng khi bắt đầu đến dòng thay đổi biến.
- Chú ý: Không cần pahir khai báo kiểu dữ liệu của biến khi khai báo, mà gán thẳng giá trị cho biến đó và nó xẽ ngầm định dạng cho kiểu biến. Không giống như các ngôn ngữ khác.
- Cú pháp khai báo biến  mảng 1 chiều: 
```
 $myArr = array("5","3","2");
 echo $myArr[2]; // truy xuất phần tử thứ 3, có giá trị hiển thị là 2
```
- Cú pháp khai báo mảng 2 chiều:
```
 $myTwoDimension = array(array(a,b,c),array(3,4,6));
 echo $myTwoDimension[0][1]; // truy xuất đến biến có giá trị hienr thị là **b**.
```

<a name="4"></a>
##4. Cấu hình Web Server
- Nếu bạn có cài một số phầm mềm khác phần mềm bạn đang cài mà chưa gỡ bỏ hoàn toàn thì nó xẽ bị lỗi xung đọt cổng với nhau khi bạn vào **localhost**.
**Chú ý** Nếu bạn bị sung đột cổng mới thay đổi còn không thì chũng ta không nên thay đổi.
- Cách giải quyết:
 + Vào thư mục **bin/apache/apache2.4.23/conf** 
 + Vào thư mục **htppd.conf** để sửa một số thông tin có liên quan về cổng.
 + Đi đến dòng có hiển thị: 

  <img src="http://imageshack.com/a/img923/5220/8leeZF.png">
 + Thay đổi:

 <img src="http://imageshack.com/a/img923/8556/ltbdTj.png">
 + Lưu lại và khỏi động lại.
 + Chúng ta thử đăng nhập vào localhost. Giờ chũng ta không đăng nhập vào đường dẫn là **localhost** mà chũng ta phải đăng nhập vào **loaclhost:30** (chúng ta đã sử thành 30).
- Thay đổi thư mục lưu trữ các code mình viết.

<a name="5"></a>
##5. Hàm phpinfo()

<a name="6"></a>
##6. Định dạng code (indentation)
- Việc PHP tự tìm ra lỗi là hơi khó nên khi ta viết mã code thì phải phân bố cục từng phần thụt ra và thụt vào hợp lý cho dễ dàng nhìn từng phần một. Để khi ta tìm lỗi hay sửa lỗi thì dễ dàng hơn.
- Chú ta có thể dùng thêm các comments để dễ hiểu từng phần hơn

<a name="7"></a>
##7. Sử dụng echo, print
- **echo**: là hàm xuất một chuỗi ra màn hình web.
- **print**: tương tụ hàm echo.
- Nhưng hàm echo dduocj sử dụng nhiều hơn.

<a name="8"></a>
##8. echo_print mã html
- Có thể Chèn PHP vào HTML để dùng hàm echo rồi in ra màn hình.
<img src="http://imageshack.com/a/img921/8999/LxZV2U.png">
- Vì bây giờ đoạn văn bản in ra là dùng theo PHP nên ta có thể chèn thêm biến bất kỳ vào trong đoạn vă bản được.
<img src="http://imageshack.com/a/img921/3218/EsOYot.png">
- Dùng if else để in ra tùy chọn:
<img src="http://imageshack.com/a/img923/4956/xTiL80.png">
- Có thể thêm css vào nữa:
<img src="http://imageshack.com/a/img921/264/jymbsA.png">
- Dấu `" " ` và dấu `' '` trong khai báo biến và trong hàm echo là tương đương nhau, chú ý là dung dấu mở nào thì phải dùng dấu đóng tương ứng.
- Để in ra dấu `'` hoăc dấu `"` nằm trong dấu tương ứng của nó thì chúng ta phải sử viết là `\'` và `\"`.
<img src ="http://imageshack.com/a/img923/7436/zILSld.png">

<a name="9"></a>
##9. Biểu thức nối chuỗi(concatenation)
- Để 2 chuỗi khi xuất ra màn hình cách nhau bởi một dấu cách thì chúng ta dùng `$bien1.' '.$bien2`. Dấu `.` có thể thay bằng dấu `,`.
<img src="http://imageshack.com/a/img924/6696/exIWoT.png">
<img src="http://imageshack.com/a/img922/3632/BEaiwW.png">
- Nối thêm một đoạn vào nữa thì dùng `$bien .= "noi dung them";`

<a name="10"></a>
##10. Nhúng PHP vào trang HTML
- Khai báo trên cùng chủ yếu nên khai bảo biến, mảng,kết nối... muốn sử dụng trong chương trình.
- Ở giữa chủ yếu để đưa ra kết quả và html format.
<img src="http://imageshack.com/a/img922/8394/ZXJAdt.png">
- Ở cuối chủ yếu dùng để hủy giá trị biến, mảng, kết nôi

<a name="11"></a>
##11. Biểu thức điều kiện if else
- Nếu trong câu điều kiện chỉ có 1 lệnh thì khong cần dấu ngoặc `{}` nếu từ 2 lệnh trở lên thì cần phải có dấu ngoặc.
- Với câu điều kiện if else lồng nhau thì phải chú ý đền các dấu ngoặc.

<a name="13"></a>
##13. Biểu thức gán
- Chungs ta có thể gán giá trị cho biến theo nhiều cách.
  + Gán thẳng cho biến luôn:
  <img src="http://imageshack.com/a/img924/741/kFkCYE.png">
  + Gán thông qua biến khác:
  <img src="http://imageshack.com/a/img922/4641/uvSlfB.png">
  + Chúng ta còn có thể gán được cả phép tóan cho biến:
  <img src="http://imageshack.com/a/img924/2075/SNLmh4.png">

<a name="14"></a>
##14. Biểu thức toán học
- Chúng ta có thể thục hiện các phép toán như trên các ngôn ngữ khác để có thể tính toán như bình thường. 
chú ý phép `/` là phép lấy giá trị nguyên, phép `%` là phép lấy số dư.

<img src="http://imageshack.com/a/img924/4691/GcoEvd.png">

<a name="15"></a>
##15. Toán tử tăng và gảm(increment and decrement operator)
- Khi chúng ta dùng `$a++ hoặc $a--` nghĩa là chúng lấy giá trị của **a** trước để in ra hoặc dùng cho các phép toán trước rồi nó mới tăng hoạc giảm giá trị cảu nó sau.
- Khi chúng ta dùng `++$a hoặc --$a` là chúng ta tăng hoạc giảm chũng trước rồi in ra hoặc dùng để tính toán.

*Chúng ta phải đặc biệt chú ý đến 2 cơ chế hoạt động cảu 2 trường hợp này*

<img src="http://imageshack.com/a/img924/4889/TZ0Esx.png">

<img src="http://imageshack.com/a/img922/7024/sAmZ2Z.png">

<a name="16"></a>
##16. Biểu thức so sánh
- So sánh giá trị của hai biến.
<img src="http://imageshack.com/a/img922/1231/OQv1k5.p">
- So sánh  kiểu dữ liệu của ha biến `===`.
<img src="http://imageshack.com/a/img923/4831/5ZeoTT.png">
<img src="http://imageshack.com/a/img923/6172/i8mxtG.png">

<a name="17"></a>
##17. Biểu thức quan hệ(logic)
- Dạng 1: biểu thức quan hệ **end** ký hiệu là `&&`.
<img src="http://imageshack.com/a/img921/2171/7QKHaN.png">
- Dạng 2: Biểu thức quan hệ **or** ký hiệu là `||`.
<img src="http://imageshack.com/a/img922/7167/T2018P.png">

<img src="http://imageshack.com/a/img922/6418/nRGMdM.png">
- Dạng 3: Biểu thức quan hệ **xor**.
<img src="http://imageshack.com/a/img921/6038/27bJIq.png">

<a name="18"></a>
##18. Hàm die và exit
- Dùng để thoát khỏi chương trình và thông báo cho người dùng biết có một lỗi nào đó. Và đưa ra lỗi cho người dùng biết.
- Ban đầu.
<img src="http://imageshack.com/a/img924/4586/M5ZHUO.png">
 + Khi cho thêm hàm `die`. Thì các dòng lệnh sau thẻ `die` sẽ không được đọc đến và k được biên dịch ra mà chỉ bien dịch và dữ lại các câu lệnh trước thẻ `die`.

 <img src="http://imageshack.com/a/img923/944/aRhUYE.png">

 + Khi cho thêm thẻ `exit`. Thì các dòng lệnh sau thẻ `exit` sẽ không được đọc đến và chỉ đọc đk những thẻ trước nó và không được lưu dữ lại àm ó sẽ thoát ra khỏi luôn.
 <img src="http://imageshack.com/a/img923/5084/Lcpj5r.png">

<a name="19"></a>
##19. Vòng lặp While và do while.
- Vòng lặp do while: Thực hiện câu lệnh trước rồi kiểm tra điều kiện, nên số lần lặp ít nhất là 1.
<img src="http://imageshack.com/a/img923/7771/0j2mFZ.png">
- Vòng lặp While: Thực hiện kiểm tra điều kiện trước sau đó mói thực hiện lệnh, nên số lần lặp ít nhất là 0.
<img src="http://imageshack.com/a/img923/7106/W3DusA.png">

<a name="20"></a>
##20. Vòng lặp for
- Vòng lặp mà chúng ta có thể kiểm xoát được biến khỏi tạo dan đầu và số vòng lăp và lặp như thế nào ngay từ đâu.
<img src="http://imageshack.com/a/img924/2610/SAUazw.png"> 

<a name="21"></a>
##21. Break và continue
- **Break**: Dừng công việc (vd như dừng vòng lặp) và thoát khỏi và không đọc các lênh phái sau.

<img src="http://imageshack.com/a/img924/5927/RRpoB8.png">
- **Continue**: Tiếp tục các câu lệnh phía sau.
<img src="http://imageshack.com/a/img924/2694/0gBJ7U.png">

<a name="22"></a>
##22. Cấu trúc rẽ nhánh Switch
- Bắt niến nào đó trong nhiều trường hợp.

<img src="http://imageshack.com/a/img924/1776/szXW1k.png">
- Chú ý: Switch chỉ so sánh bằng không có so sánh lớn hơn hoặc nhỏ hơn.

<a name="23"></a>
##23. Expression matching
- Kiểm tra tính hợp lệ của dữ liệu. Sử dụng hàm `preg_match`
- Các dùng hàm **preg_match**: `(preg_match('/ky_tu_can_tim_trong_chuoi/', $bienchuoi))`

<img src="http://imageshack.com/a/img922/7537/DTm3mF.png">
<img src="http://imageshack.com/a/img923/9702/lpgbKC.png">
- Tìm ký tự nằm trong khoảng nào đó.
<img src="http://imageshack.com/a/img923/1083/Jq1A2d.png">
<img src="http://imageshack.com/a/img922/6244/nlR0sr.png">
- Kiểm tra ký tự đầu tiên
<img src="http://imageshack.com/a/img922/360/exkWZy.png">
<img src="http://imageshack.com/a/img923/5765/o5Vaa5.png">
- Kiểm tra ký tự kết thúc
<img src="http://imageshack.com/a/img924/6122/0YFhlv.png">
<img src="http://imageshack.com/a/img923/6109/9avw9i.png">

<a name="24"></a>
##24. Hàm(fuction)

<a name="25"></a>
##25. Hàm với tham số

<a name="26"></a>
##26. Hàm với giá trị trả về

<a name="27"></a>
##27. Biến toàn cục và biến cục bộ

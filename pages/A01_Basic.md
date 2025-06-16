## **Cài đặt và Setup** 
Có thể lên các trang web để tìm đường tính hoặc lên google tìm kiếm R là có thể tải về được  
Bên cạnh ngôn ngữ R ta cũng phải cài đặt thêm RStudio nhằm để viết code theo dõi terminal cũng như có thể tạo biểu đồ trên cùng một giao diện mà không phải chuyển tab
## **R cơ bản** 
#### **Xuất**
Ta có thể sử dụng `$Nội dung cần viết` trong phần command hay terminal để chạy dòng lệnh R hay trong file đuôi .R ta cũng có thể sử dụng lệnh `print(Nội dung cần viết)` để xuất ra màn hình 
#### **Biến trong R**
Để có thể gán một giá trị cho một biến ta có thể sử dụng:
1. `=`
2. `<-`, `<--`
3. `->`, `-->`
```R
var1 = "Biến 1"
var2 <- "Biến 2"
var3 -> "Biến 3"
```
Quy tắc đặt tên biến tuân theo các quy tắc tương tự với ngôn ngữ lập trình. Tuy nhiên nên sử dụng `<-` hoặc `=` để có thể gắn một giá trị cho một biến
#### **Comment trong R**
Tương tự như Python trong R ta sử dụng `#` để thể hiện comment trong R đối với 1 câu comment còn với nhiều câu comment ta có thể chia đoạn thành các câu đơn nhỏ và sắp xếp chúng xuống hàng dần. Ngoài ra có thể sử dụng tổ hợp phím "ctrl + shift + C" để comment một đoạn nào đó
```R
## Đây là một dòng comment
```
#### **Các phép tính trong R**
##### **Phép tính toán học** 
Khi thực hiện các phép tính giữa số nguyên và số thực thì kết quả cuối cùng mà ta có được sẽ là số thực
* Phép cộng ( + ) nếu (a,b) + (c,d) -> (a+c, b+d)
* Phép trừ ( - ) tương tự như phép cộng
* Phép nhân ( * )
* Phép chia ( / )
    * Chia lấy dư ( %% )
##### **Phép tính logic**
* **Xét với các phép biểu thức đơn**
    * Phép AND ( & ) đúng khi cả hai đều đúng 
    * Phép OR ( | ) đúng nếu 1 trong hai đúng 
    * Phép NOT ( ! ) ngược lại với mệnh đề
* **Xét chung với các biểu thức**
    * Phép AND ( && ) đúng khi thành phần cả hai hai đều đúng 
    * Phép OR ( || ) đúng nếu 1 trong hai đúng 
##### **Phép tính quan hệ**
* Bé hơn ( < )
* Bé hơn hoặc bằng ( <= )
* Lớn hơn ( > )
* Lớn hơn hoặc bằng ( >= )
* không bằng ( != )
##### **Các phép tính khác**
* Kiểm tra xem giá trị có ở trong một danh sách hay không ( %in% )
* Nhân vecto ( %*% )
#### **Keyword trong R**
##### **if**
* Được sử dụng trong các câu điều kiện 
```R
if (điều kiện){
    lệnh thực hiện 
}
```
##### **else**
Xử lý điều kiện ngoại lệ của trong câu lệnh if
##### **while**
Vòng lặp thực hiện câu lệnh cho đến khi điều kiện sai 
```R
while (điều kiện dừng){
    câu lệnh lặp
    điều kiện lặp
}
```
##### **repeat**
Xử lý câu lệnh cho đến khi gặp điều kiện break 
```R
repeat {
    câu lệnh lặp 
    điều kiện lặp
    if (điều kiện dừng) break
}
```
##### **for**
Xử lý câu lệnh cho đến khi thoả điều kiện 
```R
for (điều kiện){
    câu lệnh thực hiện
}
```
##### **function**
Tạo hàm 
```R
tên hàm <- function(biến) {
    lệnh thực hiện 
    return kết quả
}
```
##### **next**
Bỏ qua câu lệnh khi đúng điều kiện 
##### **break**
Kết thúc vòng lặp
#### **TRUE/FALSE/NULL/Inf/NaN/NA**
* TRUE giá trị đúng 
* FALSE giá trị sai 
* NULL rỗng hoặc không định nghĩa Inf biểu diễn vô cực NaN biểu thị không phải dữ liệu số NA biểu diễn dữ liệu thiếu hoặc không xác định 
#### **Kiểu dữ liệu trong R**
* **Kiểu dữ liệu số trong R**
    * Khi gắn một số cho một biến trong R nó sẽ tự hiểu rằng biến được gán sẽ mang kiểu dữ liệu "double"
    * Để có thể xác định một biến thuộc lớp nào ta sẽ sử dụng hàm `class(tên biến)`  
    * Để có thể xác định một biến thuộc kiểu dữ liệu nào ta sử dụng hàm `typeof(tên biến)`
    * Để có thể xác định xem một biến có phải thuộc kiểu dữ liệu đó hay không dùng hàm `is.kiểu dữ liệu cần kiểm tra(tên biến)`
    * Để có thể chuyển đổi kiểu dữ liệu ta sử dụng hàm `as.kiểu dữ liệu cần chuyển (tên biến)`
    ngoài việc có thể chuyển đồi các kiểu đữ liệu ta cũng có thể chuyển đổi các dạng của chúng ví dụ có thể ( chuyển một vector -> một ma trận ) hay ( chuyển một vector thành một data frame )
* **Kiểu dữ liệu logic trong R**
    * TRUE đối với giá trị đúng 
    * FALSE đối với giá trị là sai   
* **Kiểu dữ liệu số phức**
    * Với ngôn ngữ R hỗ trợ kiểu dữ liệu số phức ví dụ 
```R
x <- 4 + 3i
print(class(x))
print(typeof(x))
```
**Output**
```command
[1] "complex"
[2] "complex"
```
* **Kiểu dữ liệu ký tự trong R**
Ngôn ngữ R hỗ trợ kiểu dữ liệu ký tự ( bao gồm alphabet và ký tự đặc biệt ). Mặc dù kiểu dữ liệu thông thường là string nhưng trong R vẫn được hiểu là character
* **Raw data trong R**
Để lưu trữ và làm việc với dự liệu dạng byte trong R, ta có thể sử dụng raw data. Bằng việc trình bày một loạt các byte chưa được sử lý ở định dạng thấy nhất là nhị phân
```R
x <- as.raw(c(0x1, 0x2, 0x3, 0x4))
print(class(x))
print(typeof(x))
```
**Output**
```command
[1] 01 01 03 04
```
4 thành phần trong raw vector x, mỗi số được biểu diễn thành một giá trị raw data

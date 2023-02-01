# Chapter 01

## Cơ chế hoạt động của internet
* Cơ bản, Internet là một mạng lưới các máy tính giao tiếp với nhau.
* Internet là một mạng lưới cáp vật lý toàn cầu, có thể bao gồm dây đồng điện thoại, cáp TV và cáp quang. Ngay cả các kết nối không dây như Wi-Fi và 3G / 4G cũng dựa vào các loại cáp vật lý này để truy cập Internet.
* Khi truy cập một trang web, máy tính sẽ gửi một yêu cầu qua các dây này tới một máy chủ. Máy chủ là nơi lưu trữ các trang web và nó hoạt động giống như ổ cứng máy tính. Khi yêu cầu đến, máy chủ sẽ truy xuất trang web và gửi dữ liệu chính xác trở lại máy tính.

## Giải thích về protocol của HTTP/HTTPS
* Protocol là một giao thức mạng, tập hợp các quy tắc đã được thiết lập với nhiệm vụ hàng đầu là định dạng, truyền và nhận dữ liệu. Tất cả nhiệm vụ này sẽ được thực hiện sao cho các thiết bị mạng máy tính (Từ server, router đến end point) có thể giao tiếp rõ ràng với nhau. Dù có sự khác biệt về cơ sở hạ tầng, thiết kế hay các tiêu chuẩn cơ bản thì giao thức Protocol vẫn sẽ hỗ trợ tuyệt đối để việc giao tiếp có thể diễn ra tốt nhất.
* Cơ chế hoạt động của giao thức Protocol: Các giao thức mạng thường phân chia các quy trình lớn thành nhiều phần nhỏ tương ứng với chức năng, nhiệm vụ trên tất cả cấp độ mạng. Điều này còn được biết đến là mô hình OSI được sử dụng trong mô hình tiêu chuẩn. Như vậy, ta có thể hiểu rằng sẽ có một hoặc nhiều giao thức mạng để xử lý các hoạt động trong quá trình trao đổi, sâu hơn nữa là từng lớp mạng.
    * Tầng 1: Physical Layer (Tầng vật lý), được sử dụng để truyền hoặc nhận các chuỗi bit từ các thiết bị vật lý
    * Tầng 2: Data Link-Layer (Tầng liên kết dữ liệu), là tầng có khả năng tạo khung thông tin và kiểm soát mọi luồng tin, các lỗi có thể xảy ra trong tương lai
    * Tầng 3: Network Layer (Tầng mạng), có nhiệm vụ đảm bảo mọi thông tin được trao đổi liên tục. Đồng thời, chọn đường đi, công nghệ chuyển mạch phù hợp nhất
    * Tầng 4: Transport Layer (Tầng giao vận), hỗ trợ vận chuyển thông tin giữa các máy chủ và chịu toàn bộ trách nhiệm liên quan đến việc kiểm soát các luồng, các lỗi có thể xảy ra
    * Tầng 5: Session Layer (Tầng phiên), đây là tầng thiết lập và có thể duy trì, đồng bộ hóa liên lạc giữa các thực thể. Không chỉ vậy, tầng 5 còn có chức năng loại bỏ các phiên truyền đi giữa các app
    * Tầng 6: Presentation Layer (Tầng trình diễn), chịu trách nhiệm về việc chuyển đổi thông tin, dữ liệu theo nhu cầu của các ứng dụng
    * Tầng 7: Application Layer (Tầng ứng dụng), là tầng cuối cùng và cũng là tầng giúp người dùng giao tiếp trong môi trường mạng.
* Chức năng cơ bản của giao thức Protocol 
    * Phân đoạn và hợp nhất.
    * Điều khiển liên kết.
    * Giám sát.
    * Điều chỉnh lưu lượng.
    * Phát hiện lỗi.
    * Đồng bộ hóa.

## Cơ chế hoạt động của browser và sự khác nhau giữa các browser

### Cơ chế hoạt động của browser
* Các thành phần chính của trình duyệt:
    * The user interface: bao gồm thanh địa chỉ, nút back / forward, bookmarking menu...
    * The browser engine: thực hiện các hành động tương tác giữa UI (giao diện người dùng) và rendering engine (công cụ dựng hình).
    * The rendering engine : chịu trách nhiệm hiển thị nội dung yêu cầu. Ví dụ: nếu nội dung được yêu cầu là HTML, rendering engine phân tích HTML và CSS và hiển thị nội dung lên màn hình.
    * Networking: để gửi yêu cầu, nhận phản hồi qua mạng thông qua các giao thức như HTTP, sử dụng các triển khai khác nhau đối với các nền tảng khác nhau đằng sau một giao diện độc lập với nền tảng.
    * UI backend: sử dụng để vẽ các widgets cơ bản như combo boxes và windows. Backend này cho thấy một giao diện chung không thuộc một nền tảng cụ thể. Bên dưới nó sử dụng phương thức giao diện người dùng hệ điều hành (operating system user interface methods).
    * JavaScript interpreter: sử dụng để phân tích và thực thi mã Javascript.
    * Data storage: để browsers lưu các loại dữ liệu cục bộ, chẳng hạn như cookie. Browsers cũng hỗ trợ các cơ chế lưu trữ dữ liệu như localStorage, IndexedDB, WebSQL và FileSystem.
* Cần lưu ý là các trình duyệt như Chrome chạy nhiều trường hợp của rendering engine: một cho mỗi tab. Mỗi tab chạy trong một quy trình riêng.
![Browser](https://images.viblo.asia/8586f271-89c9-4737-9ac6-77ea1eaf1bad.png)

### Sự khác nhau giữa các browser
* Tùy vào mỗi trình duyệt mà có sự khác nhau.

## Cơ chế hoạt động của DNS và domain

### Cơ chế hoạt động của DNS
* DNS là ký hiệu viết tắt của Domain Name System, nghĩa tiếng Việt là hệ thống phân giải tên miền.
* Như tên gọi của mình, chức năng chính của DNS là ‘phân giải tên miền’. Nói các khác, nó có vai trò ‘phiên dịch’ tên miền từ dạng URL quen thuộc với người dùng thành địa chỉ IP có cấu tạo 4 nhóm số quen thuộc với thiết bị mạng và ngược lại. 
* Hệ thống DNS này có cách thức hoạt hoạt động dựa theo cấu trúc truy vấn riêng. Với cấu trúc này, máy chủ DNS sẽ tự động tìm kiếm thông tin đã phân giải tại file hosts của hệ điều hành. Việc tìm kiếm có thể dẫn tới một trong hai kết quả:
    * Không thấy thông tin -> DNS tiếp tục tìm kiếm tại bộ nhớ cache
    * Không nhận được bất cứ thông tin nào -> DNS hiển thị mã lỗi. 
* DNS làm việc dựa trên nguyên tắc tra vấn hệ thống DNS server. Mỗi DNS server được vận hành, quản lý bởi một đơn vị cung cấp dịch vụ website. Theo đó, nhà cung cấp có trách nhiệm theo dõi DNS server và tên miền thương ứng. 

### Cơ chế hoạt động của domain
* Trong hệ thống internet rộng lớn thì domain chính là địa chỉ đại diện cho website của bạn. Cũng giống như số nhà của bạn trong toàn thế giới này vậy. Một domain name chỉ tồn tại cho một website. Điều này thể hiện rõ nhất qua việc khi bạn nhập vào thanh URL thì sẽ hiển thị một trang web nào đó.
* Khi bạn nhập một domain name vào thanh URL của trình duyệt web, lúc này nó sẽ gửi yêu cầu truy cập đến một mạng lưới máy chủ toàn cầu hình thành nên hệ thống domain (DNS). Sau đó các máy chủ toàn cầu này sẽ tìm kiếm các máy chủ có tên được liên kết với domain và chuyển tiếp yêu cầu đến các máy chủ tên đó.
* Domain name được tạo nên từ 2 thành phần chính gồm:
    * Tên: Là các chữ cái từ a-z, con số 0-9, dấu gạch ngang “-“, tổng số ký tự nhỏ hơn 255. Domain có có thể có dấu theo các quốc gia như domain Tiếng Việt của Việt Nam.
    * Mở rộng (Đuôi) domain bắt đầu bằng dấu “.” và bao gồm những phần mở rộng.

## Giải thích về hosting server
* Hosting là giải pháp chuyển chi phí bảo trì phần cứng và nhân sự sang điện toán đám mây. Việc chọn đúng một công ty cung cấp hosting là cực kỳ quan trọng đối với sự thành công của công ty bạn. Hosting Servers có tác động khá lớn tới lợi nhuận, vì nó ảnh hưởng trực tiếp đến phần doanh số của bạn. 
* Hosting bạn chọn sẽ phụ thuộc vào trang web bạn muốn chạy và số lượng khách truy cập bạn mong đợi. Xác định các service bạn muốn cho trang web của mình trước khi nghiên cứu các dịch vụ server host.
* Hosting Servers là việc quản lý offsite và duy trì các tài nguyên phần cứng được chỉ định cho việc sử dụng của công ty. Bằng cách trả phí hàng tháng cho dịch vụ hosting, các công ty có thể thu được lợi ích từ việc có cơ sở hạ tầng CNTT đầy đủ, mà không phải trả chi phí liên quan đến bảo trì, đào tạo và cập nhật thiết bị.
* Phần chi phí cho phần cứng server và thuê nhân viên IT ở các doanh nghiệp nhỏ khá hạn chế. Một doanh nghiệp muốn một máy chủ riêng có thể phải chi hàng nghìn đô la để mua những phần cứng. Chi phí lắp đặt tại chỗ , trang bị bảo mật và phương án dự phòng. Cùng với đó bạn cần có một nhân viên CNTT đủ giỏi để đảm bảo chức năng của Servers ổn định. Nhu cầu về một máy chủ nhanh chóng tăng lên, từ một khoản đầu tư nhỏ cho phần cứng lên đến con số rất lớn và nguồn lực liên tục.
* Bằng cách tranh thủ sự trợ giúp của dịch vụ server hosting. Các doanh nghiệp loại bỏ được nhu cầu giữ tài nguyên máy chủ tại chỗ. Họ không phải bảo trì phần cứng, đảm bảo duy trì hoạt động của nó hoặc thậm chí lo lắng về việc khắc phục sự cố trong thời điểm khủng hoảng. Dịch vụ hosting đảm bảo mọi thứ để chắc chắn máy chủ luôn sẵn sàng khi công ty cần.
* Giải pháp Hosting Servers điển hình bao gồm managed hosting (máy chủ riêng), máy chủ riêng ảo và máy chủ chuyên dụng.

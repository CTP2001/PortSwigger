# Username enumeration via different responses

* Trước tiên ta đăng nhập một tài khoản bất kỳ để để lấy được request `POST /login`.
![Capture01](https://hackmd.io/_uploads/rJLix58Lp.png)

* Sau đó ta gửi request `POST /login` ở trên tới Burp Intruder và thêm payload có giá trị của username.
![Capture02](https://hackmd.io/_uploads/ByE2g9I8p.png)

* Ta tiến hành brute-force với danh sách các username đã cho sẵn. Kết quả trả về như hình dưới, ta tìm được một username có nội dung response trả về khác với các username còn lại. Nội dung response là `Incorrect password`, nghĩa là username này có tồn tại trong hệ thống.
![Capture03](https://hackmd.io/_uploads/SJNne58LT.png)

* Sau khi có được username, ta tiến hành brute-force tiếp password.
![Capture04](https://hackmd.io/_uploads/S1E2x5IL6.png)

* Kết quả trả về có status code là `302`, đây chính là password cần tìm.
![Capture05](https://hackmd.io/_uploads/rk42lq8LT.png)

* Đăng nhập bằng username và password đã tìm được. Hoàn thành bài lab.
![Capture06](https://hackmd.io/_uploads/SyN3x5ULp.png)



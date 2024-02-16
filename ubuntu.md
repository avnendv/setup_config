- Kiểm tra ubuntu info

  ```
  lsb_release -a
  ```

- Kiểm tra trạng thái sử dụng ram

  ```
    free -m
  ```

- Kiểm tra còn trống bao nhieu disk

  ```
    df -h /
    or
    top // giống task manager trên win
  ```

- Đổi name server

  ```
    sudo hostnamectl set-hostname update-name-server

    // reboot lại server sau khi đổi tên
    sudo reboot
  ```

- Kiểm tra các cổng trên server

  ```
    netstat - tlpun
  ```

- Kiểm tra các tiến trình đang chạy trên hệ thống

  ```
    ps -ef
  ```

- Kiểm tra server có thông kết nối với server khác không

  ```
    telnet ip port

    traceroute -T -p port ip // kiểm tra đường truyền có bị chặn ở đâu k
  ```

- Tạo user
  ```
    sudo useradd user-name // chỉ tạo user
    sudo adduser user-name // tạo user vs các chỉ định thông tin user
  ```
- Chuyển user

  ```
    su user-name
  ```

- Kiểm tra thông tin user

  ```
    vi /etc/passwd
  ```

- Xóa user

  ```
    deluser user-name
  ```

- Tạo group

  ```
    groupadd group-name

    // xóa
    delgroup group-name
  ```

- Add user vào group

  ```
    usermode -aG group-name user-name // ko có option G thì sẽ thêm user vào group và xóa các group trước đó của user
  ```

- Kiểm tra group của user

  ```
    groups user-name
  ```

- Xóa user khỏi group

  ```
    deluser user-name group-name
  ```

- Phân quyền

  ```
    ls -l dir // thông tin về quyền của dir/
    chown user-name(chủ sở hữu):group-name(nhóm sở hữu) dir/
    chown -R user-name(chủ sở hữu):user-name(nhóm sở hữu) dir/ // áp dụng thay đổi cho cấp con

    // các quyền trên ubuntu  r(read) w(write) x(execute)
    // các quyền đc sắp xếp ugo (user - group - other)
    // thay đổi quyền
    chmod g=rwx dir/ | chmod u=rwx,g=rx,o=- dir/

    // quyền bằng số r=4 w=2 x=1
    chmod 750 dir/
  ```

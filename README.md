## Tiền triển khai
Tạo ra các file ssh key trong thư mục EC2
```
ssh-keygen
```
## Triển Khai
1. Khởi tạo dự án Terraform:
   ```
   terraform init
   ```

2. Xem trước các thay đổi sẽ được thực hiện:
   ```
   terraform plan
   ```

3. Triển khai cơ sở hạ tầng:
   ```
   terraform apply
   ```

4. Xóa cơ sở hạ tầng khi không cần thiết:
   ```
   terraform destroy
   ```

## Lưu Ý
- Luôn kiểm tra kỹ các thay đổi với `terraform plan` trước khi thực hiện `terraform apply`.
- Sử dụng `terraform state` để quản lý trạng thái của cơ sở hạ tầng.
- Đảm bảo bảo mật thông tin nhạy cảm trong tệp `terraform.tfvars`.

Hy vọng hướng dẫn này sẽ giúp bạn triển khai Terraform một cách dễ dàng và hiệu quả. Chúc bạn thành công!
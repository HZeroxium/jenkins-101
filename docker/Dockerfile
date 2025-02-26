# Sử dụng Jenkins inbound-agent làm base image
FROM jenkins/inbound-agent:jdk17

# Cập nhật package list và cài đặt Python3, pip
USER root
RUN apt-get update && apt-get install -y python3 python3-pip && \
  apt-get clean && rm -rf /var/lib/apt/lists/*

# Xác nhận phiên bản đã cài đặt
RUN java -version && python3 --version && pip3 --version

# Chuyển lại quyền về user Jenkins để tránh lỗi bảo mật
USER jenkins

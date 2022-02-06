# Application for attendance by facial recognition
Computer Vision final assignment

## Requirements
- [face_recognition](https://github.com/ageitgey/face_recognition)
- Flask framework to build web app


## Requirements
- face_recognition
- Flask

## How to install face_recognition library
- Visit [face_recognition](https://github.com/ageitgey/face_recognition) for detail
- Following is my way to install face_recognition library in Windows

        conda update ipykernel
        conda update --all

        repeat the above update till no error (took few runs for me), then run:

        conda create -n face_recognition python==3.6.6 anaconda
        conda activate face_recognition
        pip install cmake
        pip install dlib==19.8.1
        pip install face_recognition
        pip install opencv-contrib-python==4.1.0.25
        pip install twisted

- cre: https://github.com/ageitgey/face_recognition/issues/175#issuecomment-636287794


## How to run
- Run with cmd:
- `cd` to project directory
- `set FLASK_APP=diemdanh`
- `set FLASK_ENV=development`
- Init database before run (optional): `flask init-db`
- `flask run`

## Các chức năng

- Hệ thống hiện tại chỉ có hai chức năng: “Thêm sinh viên” và “điểm danh”. 

+ Thêm sinh viên

![image](https://user-images.githubusercontent.com/59023235/152696192-c7e35c14-ac8d-480c-98f4-41f976ae2dd1.png)

Người quản lý thêm sinh viên bằng cách điền tên và thêm ảnh của họ. Sau đó hệ thống sẽ generate ra vector encoding face (128 chiều) để sau này tiện so khớp. Người quản lý cũng có thể xoá sinh viên. Trên hình ảnh, cột “encoding face” được hiển thị ra để tiện theo dõi trong quá trình debug, ngoài ra không có tác dụng gì thêm. 

+ Điểm danh

![image](https://user-images.githubusercontent.com/59023235/152696216-e7342e55-ec67-4f3e-b91e-6ef5a8a9e632.png)


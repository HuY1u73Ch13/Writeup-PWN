![image](https://github.com/user-attachments/assets/749b0f09-acb9-484e-b970-1dfbe1737059)![image](https://github.com/user-attachments/assets/362d5b7d-e00d-4587-8c27-dec937e15652)![image](https://github.com/user-attachments/assets/eaa2aa7a-3e7a-4bb8-b9c4-e58b44e2160a)![image](https://github.com/user-attachments/assets/38ede511-12c4-4a7e-bb71-22f1213fa4df)
* Đầu tiên đọc code ta thấy biến buf khai báo 28 byte nhưng lại nhập vào tận 48 byte như vậy ta có lỗi Buffer_Overflow ở đây
![image](https://github.com/user-attachments/assets/cfa7f7d3-0cdd-4e6f-85bd-a2e33beb0b55)
* Đặt break_point tại hàm read hàm read.
* Hàm read cho chúng ta nhập vào 48 byte nên chúng ta thử nhập 48 byte coi nó tràn được đến đâu
![image](https://github.com/user-attachments/assets/5510eef0-4053-487f-b6d6-51bdbea2d339)
![image](https://github.com/user-attachments/assets/2b2e509b-0f3c-4706-9c7a-b210ecbad575)
* Đi đến hàm return ta thấy nó đã ơverdrive đến địa chỉ 0x00007fffffffe118
* Vậy bây giờ mình cần tìm offset nó để overdrive đến cái mình muốn
![image](https://github.com/user-attachments/assets/8727f3d7-c7b9-4a00-a8b0-62a4fdc6e371)
* Ở hàm return ta thấy hàm tiếp theo nó sẽ chạy vào hàm 0x00007ffff7db6d00 nhưng chúng ta phải overdrive vào hàm win đấy là mục đích của thử thách này
* 



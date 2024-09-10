# QuestaSim + GTKwave Guideline

# I. Cách cài đặt QuestaSim

## 1. Window

<aside>
📎

Link cài đặt: [https://downloadly.ir/software/engineering-specialized/mentor-graphics-questasim/](https://downloadly.ir/software/engineering-specialized/mentor-graphics-questasim/)

</aside>

- **Lưu ý:**
    - Chọn phiên bản phù hợp với cầu hình máy cá nhân
    - Làm từng bước theo video sau: https://www.youtube.com/watch?v=WgyNRYXe2dc&t=17s
    - Cố gắng cài vào các đường dẫn trong ổ :/C vì cài các ổ khác đã từng xuất hiện lỗi

## 2. Ubuntu

<aside>
💡

Link cài đặt: [QuestaSIM_ubuntu](https://drive.google.com/drive/folders/12tQXvh8veksHScQ6VrZCLLe9KkT6B7Yr?fbclid=IwY2xjawFL3S1leHRuA2FlbQIxMAABHQ7Nz02Jscba9LGLournPpAfjl2eYbLoSPg-3CxS7Je_UTez0DhggsQqXg_aem_ZZUsoBI9JJzbtVwotUjMkQ)

</aside>

1. **Dowload file nén 1.5GB và giải nén**
2. **Mở Terminal tại folder Mentor Graphics QuestaSim 10.7c Linux64**

![[[image1](questa_gtkw_tutorial/images/image 1.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%201.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image.png)

1. **Make file executable:** 

```bash
chmod +x install.linux64
./install.linux64
```

Sau khi chạy 2 lệnh này màn hình sẽ hiển thị GUI như sau:

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%201.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%201.png)

1. **Cài đặt**
- Bấm INSTALL
- Chọn đường dẫn cài đặt

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%202.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%202.png)

- Chọn cả 2 mục sau ở phần Releases

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%203.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%203.png)

- Chọn All Platform

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%204.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%204.png)

- Chọn hết phần Selection

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%205.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%205.png)

- AGREE ở mục EULA ⇒ Cuối cùng bấm Install

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%206.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%206.png)

1. **Crack QuestaSim**
- Copy 3 files (MentorKG.exe, MGLS.DLL, Patch_DownLoadLy.iR.bat) từ folder
Crack/Others/2 và Paste vào ../questasim/linux_x86_64.

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%207.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%207.png)

- Cài wine: Link: [https://gitlab.winehq.org/wine/wine/-/wikis/Debian-Ubuntu](https://gitlab.winehq.org/wine/wine/-/wikis/Debian-Ubuntu) hoặc xem bên dưới đây

```bash
sudo dpkg --add-architecture i386
cat /etc/os-release
sudo mkdir -pm755 /etc/apt/keyrings
sudo wget -O /etc/apt/keyrings/winehq-archive.key https://dl.winehq.org/wine-builds/winehq.key
# Nếu là ubuntu 20.04
sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/focal/winehq-focal.sources
sudo apt update
sudo apt install --install-recommends winehq-stable
```

- Mở Terminal trong folder **linu_x86_64**, sau đó chạy file Patch_DownLoadLy.iR.bat với wine. Sau khi GUI wine hiện ra, bấm INSTALL

```bash
chmod +x Patch_DownLoadLy.iR.bat
wine Patch_DownLoadLy.iR.bat
```

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%208.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%208.png)

- Sau khi chạy xong, file LICENSE.TXT sẽ hiện ra, uncomment 2 dòng đầu tiên và thêm đường dẫn vào sau dòng thứ 2

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%209.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%209.png)

- Góc trái bên trên, chọn File ⇒ Save As ⇒ Lưu tại folder /questasim với tên **LICENSE.dat**
- Mở Terminal gõ lệnh:

```bash
gedit ~/.bashrc
```

- Tại file bashrc, thêm 2 đường dẫn: (dấu … là đường dẫn còn lại, bạn hãy sử dụng lệnh pwd để lấy đường dẫn tuyệt đối tại địa chỉ bạn đang đứng, sau đó paste vào bashrc)

```bash
export PATH=$PATH:.../questasim/bin/
export LM_LICENSE_FILE=.../questasim/LICENSE.dat 
```

- Sau đó chạy lệnh

```bash
source ~/.bashrc
```

- Download SFK: [http://stahlworks.com/downloads.html](http://stahlworks.com/downloads.html) download file SFK for Linux
(i686 64 bits executable)

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%2010.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%2010.png)

- Chuyển file sfk-linux-64.exe tới folder /questasim
- Mở Terminal tại đường dẫn ../questasim và chạy các lệnh sau

```bash
chmod +x sfk-linux-64.exe
# Đoạn này hay lỗi, mình khấn các cụ nha <3
sudo apt install winetricks
sudo wine ./sfk-linux-64.exe rep -yes -pat -bin
/5589E557565381ECD00000008B5508/31C0C357565381ECD00000008B5508/ -bin
/5589E557565381ECD8000000E8000000005B81C3/33C0C357565381ECD8000000E8000000005B81C3/ -bin
/41574989FF415641554154554889CD534489C3/33C0C389FF415641554154554889CD534489C3/ -dir
/home/ttduong/workspace/questasim
```

- Lỗi:
    
    ![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%2011.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%2011.png)
    
    - Sửa: sử dụng lệnh sau: (nhớ thay đổi đường dẫn theo đường dẫn trên máy)
    
    ```bash
    sudo wine ./sfk-linux-64.exe rep -yes -pat -bin /5589E557565381ECD00000008B5508/31C0C357565381ECD00000008B5508/ -bin /5589E557565381ECD8000000E8000000005B81C3/33C0C357565381ECD8000000E8000000005B81C3/ -bin /41574989FF415641554154554889CD534489C3/33C0C389FF415641554154554889CD534489C3/ -dir /home/ttduong/workspace/questasim
    ```
    
    
- Nếu thành công, màn hình sẽ hiện như sau:

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%2012.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%2012.png)

- Màn hình yêu cầu cài cái gì thì mình cài bổ sung. Nếu không có, màn hình sẽ báo như trên ⇒ Ctrl + C để ngắt

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%2013.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%2013.png)

- Cài LSB và chạy lệnh sau

```bash
sudo apt install lsb
sudo ./linux_x86_64/mgls/bin/lmgrd -c ./LICENSE.dat
```

- Chú ý:
    - Nếu gặp lỗi: Can’t make directory usr/tmp/.flexlm, errno: 2(No such file or directory)
    
    ⇒ Chạy lệnh: *sudo ln -s /tmp /usr/tmp*
    
    - Nếu gặp lỗi: (lmgrd) Failed to open the TCP port number in the license.
      
    → Open file LICENSE.dat → replace 27001 to 27002 (if still failed, 2700(3, 4, 5, …))
  
- Nếu thành công màn hình sẽ hiện như sau:

![[image.png](QuestaSim%20+%20GTKwave%20Guideline%208fbb5a1bb36b43939404ff3083c8e484/image%2014.png)](https://github.com/ttDuong282/questa_gtkw_tutorial/blob/main/images/image%2014.png)

# Một số lệnh phổ biến khi sử dụng QuestaSim

```bash
# Lệnh chạy GUI questasim
vsim
# Lệnh compile Verilog code hoặc Systemverilog extensions
vlog <tên_file_code>.v <tên_file_code>.sv 
# Lệnh restart các thông số thiết kế đã innitialize trong 
# quá trình mô phỏng, reset lại thời gian
restart
# Lệnh chạy toàn bộ quá trình mô phỏng (ngoài ra nếu muốn chạy với các options
# khác, sử dụng -help để tra cứu
run -all

```

# II. Cách cài đặt GTKwave

## Cài đặt

```bash
sudo apt update
sudo apt install gtkwave
```

## Lệnh sử dụng

```bash
gtkwave <tên_file>.vcd
```

# III. Tham khảo

## Các thao tác trong QuestaSim

[thaotac_questasim](https://nguyenquanicd.blogspot.com/2019/03/questa-simuvm-huong-dan-co-ban-e-su.html)

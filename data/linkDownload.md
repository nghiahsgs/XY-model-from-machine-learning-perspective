##Delta=0.2 (L=12,16,24,32,40,48,56,64)
https://drive.google.com/drive/folders/1vASzFrJBuOA8gw4dxPNlSYBKwktYa53q

##Delta=0.34 (L=12,16,24,32,40,48,56,64)
https://drive.google.com/drive/folders/1QQLDsjrM3sgqkImZhP85N1VBw70EwAOn


##Delta=0.7 (L=12,16,24,32,64)
https://drive.google.com/drive/folders/1H5iyhSRX3lGwFMUWLGBZlhKhdNK5SmwB

##Delta=1.0 (L=12,16,24,32,40,48,56,64)
https://drive.google.com/drive/folders/1Q3rUxHsuznNKaxyfok30uYFcmzRQsFxb

<br>Bên trong mỗi thư mục của mỗi Delta và  mỗi L sẽ có 20 file h5 run01.h5 đến run20.h5.

<br> Bên trong mỗi file h5 chứa các điểm dữ liệu (các data point), thông tin mõi data point bao gồm: cấu hình spin của data point đó (mảng 2 chiều L x L) ; label của data point đó; nhiệt độ của datapoint đó; L : kích thước mô phỏng 


<br> (demo) code python đọc dữ liệu từ file h5
import h5py
f=h5py.File('run01.h5','r')
L=f['L'][()]
print(L)

//cấu hình của một datapoint
f['3029917']['config'][()] //3029917 là 1 key ngẫu nhiên lấy từ f.keys()

//nhiệt độ
f['3029917']['T'][()]

//label của data point (int)
f['3029917']['label'][()]





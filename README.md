# Building a Data Warehouse for Universities to propose strategies to improve rankings on U-MULTIRANK
CREATE TABLE TIME(
MATG nvarchar(10) not null PRIMARY KEY,
NAM int,
THANG int
)

CREATE TABLE HOATDONGXAHOI(
MAHDXH nvarchar(20) not null PRIMARY KEY,
TENHDXH nvarchar(300),
DONVITOCHUC nvarchar(100)
)
CREATE TABLE DOITAC(
MADOITAC nvarchar(20) not null PRIMARY KEY,
TENDOITAC nvarchar(100),
MAKV nvarchar(20) 
)

CREATE TABLE KHUVUC(
MAKV nvarchar(20) not null PRIMARY KEY,
TENKHUVUC nvarchar(100),
QUOCGIA nvarchar(100)
)
CREATE TABLE NGANH(
MANGANH nvarchar(20) not null primary key,
TENNGANH nvarchar(100),
MAKHOA nvarchar(20) 
)

CREATE TABLE KHOA(
MAKHOA nvarchar(20) not null primary key,
TENKHOA nvarchar(100)
)

CREATE TABLE NCKH(
MANC nvarchar(20) not null primary key,
TENDETAI nvarchar(200),
MALINHVUC nvarchar(20),
MATHELOAI nvarchar(20),
CONGBO nvarchar(10)
)

CREATE TABLE LINHVUCDETAI(
MALINHVUC nvarchar(20) not null primary key,
TENLINHVUC nvarchar(100)



)

CREATE TABLE THELOAIDETAI(
MATHELOAI nvarchar(20) not null primary key,
TENTHELOAI nvarchar(200)
)
CREATE TABLE THONGTINSINHVIEN(
MASV nvarchar(20) not null primary key,
HOTENSV nvarchar(150),
NGAYSINH nvarchar(50),
GIOITINH nvarchar(20),
NIENKHOA nvarchar(50),

MATRANGTHAI nvarchar(20)
)
CREATE TABLE TRANGTHAISV(
MATRANGTHAI nvarchar(20) not null primary key,
TENTRANGTHAI nvarchar(100)
)

CREATE TABLE XEPLOAI(
MAXEPLOAI nvarchar(20) not null primary key,
TENXEPLOAI nvarchar(100)
)

CREATE TABLE TRAODOISINHVIEN(
MATDSV nvarchar(20) not null primary key,
TENCHUONGTRINH nvarchar(200)
)
CREATE TABLE THONGTINGV(
MAGV nvarchar(20) not null primary key,
HOTENGV nvarchar(150),
NGAYSINH nvarchar(50),
GIOITINH nvarchar(20),
MAHOCVI nvarchar(50),
)

CREATE TABLE HOCVI(
MAHOCVI nvarchar(50) not null primary key,
TENHOCVI nvarchar(100)
)

CREATE TABLE TRAODOIGIANGVIEN(
MATDGV nvarchar(20) not null primary key,
TENCHUONGTRINH nvarchar(200)
)


CREATE TABLE KHUVUCTRAODOI(
MAVITRI nvarchar(20) not null primary key,
CHAULUC nvarchar(100),
QUOCGIA nvarchar(100),
TRUONG nvarchar(200)
)
CREATE TABLE FACT_SV(
MASV nvarchar(20),
MATDSV nvarchar(20),
MAXEPLOAI nvarchar(20),
MANGANH nvarchar(20),
MATG nvarchar(10),
MAVITRI nvarchar(20),
GPA FLOAT
)

CREATE TABLE FACT_GV(
MAGV nvarchar(20),
MANC nvarchar(20),
MANGANH nvarchar(20),
MATDGV nvarchar(20),
MATG nvarchar(10),
MAVITRI nvarchar(20),
DIEMBAINCKH float,
CHISOTRICHDAN int

)

CREATE TABLE DAOTAOVAPHATTRIEN(
MATG nvarchar(10),
MANGANH nvarchar(20),
MADOITAC nvarchar(20),
MAHDXH nvarchar(20),
SOLUONGSV int,
DOANHTHU int
)

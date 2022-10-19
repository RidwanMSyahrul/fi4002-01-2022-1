# 10219040
NamaLengkap


## materi sebelumnya
+ Euler 
+ Runge-Kutta orde 4
+ Transformasi Fourier
+ Monte Carlo
+ Rekursif
+ Lotka Volterra
+ Heat Diffusion Model
+ Osilasi Bandul (Overdamped, Critically Damped, Underdamped) 
+ Penyelesaian Persamaan ODE (Ordinary Differential Equation) 



## materi paling menarik
+ Monte Carlo
+ Osilasi Bandul


## materi paling membosankan
+ Euler
+ Heat Diffusion Model


## materi yang sudah dipahami
+ Runge Kutta orde 4
+ Heat Diffusion Model
+ Osilasi Bandul


## materi yang belum dipahami
+ Monte Carlo
+ Transformasi Fourier
+ Euler (masih suka bingung untuk persamaannya) 


## contoh program
+ Buat suatu contoh program dalam Python dan sertakan di sini dengan hasil keluarnnya.

```python
# contoh program python
import numpy as np
import matplotlib.pyplot as plt

def koch_snowflake(order,scale =10):
	def _koch_snowflake_complex(order):
		if order == 0:
			angels = np.array([0,120,240])+90
			return scale/np.sqrt(3)*np.exp(np.deg2rad(angels)*1j)
		else:
			ZR = 0.5-0.5j*np.sqrt(3)/3
				
			p1= _koch_snowflake_complex(order-1)
			p2 = np.roll(p1, shift=-1)
			dp=p2-p1
				
			new_points = np.empty(len(p1)*4, dtype=np.complex128)
			new_points[::4]=p1
			new_points[1::4]=p1+dp/3
			new_points[2::4]=p1+dp*ZR
			new_points[3::4]=p1+dp/3*2
			return new_points
	points=_koch_snowflake_complex(order)
	x, y = points.real, points.imag
	return x, y
	
	
	
x, y= koch_snowflake(order=10)

plt.figure(figsize=(8, 8))
plt.axis('equal')
plt.fill(x, y)
plt.show()
```

Hasilnya adalah

```

```


## cara perkuliahan
+ Penyampaian materi sudah baik, dan penggunaan waktu kuliah pun sudah sesuai. Saran untuk kedepannya mungkin materi dibagikan juga dalam bentuk pdf atau contoh programnya juga diberikan agar mahasiswa bisa belajar kembali. 


## topik sistem fisis
+ Pergerakan atom dalam struktur kristal yang memiliki cacat


## simulasi dan visualisasi
+ Saya tertarik untuk melakukan simulasi dan visualisasi. Topik yang ingin divisualisasikan adalah pergerakan atom dalam kristal serta ikatan yang terjadi didalamnya. 

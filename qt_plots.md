

## Previous mistakes

In the figure below:
The right column is the figure I often show to you. The condensation rate in the y (cross mountain) direction. The left column shows two contours. 
1. qvb_cond_sk means qvb_cond filtered by sk (dash). 
2. xs_cond_sk means xs_cond filtered by sk (solid). 

I made mistakes here, the qvb_cond doesn't need to be fitered by the w when we apply sk to the condensation rate. The difference between the left column and right column is due to the way I deal with the positiev qvb_mp values( evaporation )

1. in the left column, I use 'nan' to replace positive qvb_mp values, then apply nanmean 
2. in the right column, I use '0' to replace positive qvb_mp values, then apply nanmean

In the left column: replace evporation values with 'nan' is alsolutely wrong.

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qvb_xs_cond_detail.png)


To better explain the reason why nanmean is wrong, the figure below instead of the time mean, the snapshot is provioded.

* In the left column, We can see large condensation areas besides the two known maxima. The large value can be caused by less number to average in x direction (neglect nan).

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qvb_xs_cond_detail.png)



## Qt tendencies

### the unit of below contour plots is mm per second
### qt_cond
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_cond_no_weighted.png)

### qt_dep
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_dep_no_weighted.png)

### qt_evar
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_evar_no_weighted.png)

### qt_evac
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_evac_no_weighted.png)

### qt_sub
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_sub_no_weighted.png)

### qt_evar and qt_evac
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_evar_evac_no_weighted.png)

### qt_subl and qt_dep 
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_subl_dep_no_weighted.png)

## simple qt analysis

### vertical integration of qt

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_2d_analysis.png)


## different condensation rate analysis
1. cond rate from qvb_mp
2. cond rate from qt
3. cond rate from XS equations qci thershold=10 e -6
4. cond rate from XS equations qci threshold=10 e -6

### Different cond rate types in the same warming scenario

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_compare1.png)

#### different warming scenarios for the same cond rate type

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_compare2.png)

#### condensation change not normalize by temperature

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_increasement_compare.png)

#### condensation change normalize by temperature

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_increasement_compare_normalize.png)

## The difficulties in defining the area used to calculate the Precipitation efficiency

not clear how to connect the PE with rain rate. 

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/how_to_select_pe_region.png)


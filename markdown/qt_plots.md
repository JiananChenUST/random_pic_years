

## Previous mistakes

>    In the figure below:

> ![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qvb_cond_detail_contour_20_levels_2.png)


I made mistakes here, the qvb_cond doesn't need to be fitered by the w when we apply sk to the condensation rate. The difference between the left column and right column is due to the way I deal with the positive qvb_mp values( evaporation )

1. in the left column, I use 'nan' to replace positive qvb_mp values, then apply nanmean 
2. in the right column, I use '0' to replace positive qvb_mp values, then apply nanmean

In the left column: replace evporation values with 'nan' is alsolutely wrong.




To better explain the reason why nanmean is wrong, the figure below instead of the time mean, the snapshot is provioded.

* In the left column, We can see large condensation areas besides the two known maxima. The large value can be caused by less number to average in x direction (neglect nan).

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qvb_weighted_or_not_in_t_series.png)



## Qt tendencies

### the unit of below contour plots is mm per second,note I didn't interp these on height levels just on the model levels. The interpolation on height leveles can be soon implemented if needed.
### qt_cond
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_cond_no_weighted.png)

### qt_dep
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_dep_no_weighted.png)

### qt_evar
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_evar_no_weighted.png)

### qt_evac
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_evac_no_weighted.png)

### qt_sub
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_subl_no_weighted.png)

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
4. cond rate from XS equations qci threshold=10 e -5

### Different cond rate types in the same warming scenario

#### qt_cond
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_compare1.png)

#### qt_dep+ qt_cond
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_compare1_dep.png)

#### different warming scenarios for the same cond rate type

#### qt_cond
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_compare2.png)

#### qt_dep+ qt_cond
![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_compare2_dep.png)

#### condensation change not normalize by temperature

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_increasement_compare.png)

#### condensation change normalize by temperature

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_increasement_compare_normalize.png)

## The difficulties in defining the area used to calculate the Precipitation efficiency

not clear how to connect the condensation rates with rain rate. different condensations rates are plotted here.

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/how_to_select_pe_region.png)

## Domain wide condensation comparison based on different condensation rate types
### Our XS condensation rate sensitivity is smaller compared with qt_cond rate and qvb_cond rate

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/cond_domain_wide.png)

### qt_cond and qt_dep 

qt_cond and qt_dep is better at approximating to the qvb_mp

![test](https://github.com/JiananChenUST/random_pic_years/blob/main/qt_cond_dep_domainwide.png)
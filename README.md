## AreaPicker
[ ![Download](https://api.bintray.com/packages/chenenyu/maven/area-picker/images/download.svg) ](https://bintray.com/chenenyu/maven/area-picker/_latestVersion)

可定制的省市县选择器!

## Features

* 采用[DialogFragment](http://developer.android.com/intl/zh-cn/reference/android/app/DialogFragment.html)实现,生命周期跟随Activity,不会因为屏幕旋转等因素而自动消失.
* 历史记录存储,上次完成的操作会在本次操作中标记出来.
* 支持省份选择(PickLevel.PROVINCE_ONLY)、省市联动(PickLevel.PROVINCE_CITY)、省市县联动(PickLevel.ALL  默认)

## How to use
	In your build.gradle:
	dependencies {
    	compile 'com.chenenyu.areapicker:lib:1.0.1'
	}
	
	Then:
	FragmentTransaction ft = getSupportFragmentManager().beginTransaction();
	Fragment prev = getSupportFragmentManager().findFragmentByTag("dialog");
	if (prev != null) {
    	ft.remove(prev);
	}
	ft.addToBackStack(null);
	picker = new AreaPicker();
	// 支持省份/省市/省市县联动
	//picker.setLevel(PickLevel.PROVINCE_CITY);
	picker.show(ft, "dialog");
	

见demo.



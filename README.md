# LineChart
![image](https://github.com/WelliJohn/LineChart/blob/master/imgs/shitu.gif)

<b>使用example:</b>
1.初始化数据：<br>
//y轴的点<br>
private double[] mYdots = new double[]{0, 5, 10, 15, 20, 25, 30, 35, 40};<br>
//x轴的点<br>
private String[] mXdots = new String[]{"08/18", "08/19", "08/20", "08/21", "08/22", "08/23", "08/24",
            "08/25", "08/26", "08/27", "08/28", "08/29", "09/01", "09/02", "09/23"};<br>

//在布局中写的ChartLine<br>
<wellijohn.org.linechart.chartline.ChartLine
        　　android:id="@+id/chartLine"
        　　android:layout_width="wrap_content"
        　　android:layout_height="wrap_content"
        /><br>
private ChartLine mChartLine;<br>


//显示的坐标点,通过这些坐标点进行连线<br>
private List<DotVo> mListDisDots;<br>

//构造显示的点数据<br>
private void initTestData() {<br>
　　　　　　mListDisDots = new ArrayList<>();<br>
        　　DotVo tempDotVo = new DotVo("08/18", 5);<br>
        　　mListDisDots.add(tempDotVo);<br>
        　　DotVo tempDotVo1 = new DotVo("08/19", 10);<br>
        　　mListDisDots.add(tempDotVo1);<br>
        　　DotVo tempDotVo2 = new DotVo("08/20", 7);<br>
        　　mListDisDots.add(tempDotVo2);<br>
        　　DotVo tempDotVo3 = new DotVo("08/21", 15);<br>
        　　mListDisDots.add(tempDotVo3);<br>
        　　DotVo tempDotVo4 = new DotVo("08/22", 23);<br>
        　　mListDisDots.add(tempDotVo4);<br>
        　　DotVo tempDotVo5 = new DotVo("08/23", 40);<br>
        　　mListDisDots.add(tempDotVo5);<br>
        　　DotVo tempDotVo6 = new DotVo("09/02", 0);
        　　mListDisDots.add(tempDotVo6);

}

<b>2.设置数据，并显示</b>
try {
    mChartLine.setYdots(mYdots).setXdots(mXdots).setListDisDots(mListDisDots).reDraw();
} catch (YCoordinateException e) {
    e.printStackTrace();
}

3.现在只是写个设计思路，目前由于ui还没出来，可以慢慢定制，等ui好了，会封装成jar上传至jcenter.






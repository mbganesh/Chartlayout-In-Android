# Chartlayout-In-Android
This Repo show you Animated Pie Chart in android


Java File Code:
**************
 pieChart = view.findViewById(R.id.pieChartMaths);
        qn_ans = view.findViewById(R.id.qa_maths);
        vdo_watch = view.findViewById(R.id.vw_maths);
        points = view.findViewById(R.id.pe_maths);

        int a = Integer.valueOf(qn_ans.getText().toString());
        int b = Integer.valueOf(vdo_watch.getText().toString());
        int c = Integer.valueOf(points.getText().toString());

        ArrayList<PieEntry> NoOfEmp = new ArrayList<>();
        NoOfEmp.add(new PieEntry(a, 1));
        NoOfEmp.add(new PieEntry(b, 2));
        NoOfEmp.add(new PieEntry(c, 3));

        PieDataSet dataSet = new PieDataSet(NoOfEmp, "Maths Analysis");

        PieData data = new PieData(dataSet);
        pieChart.setData(data);
        dataSet.setColors(ColorTemplate.COLORFUL_COLORS);
        pieChart.animateXY(1000, 1000);
        
        
XML Code:
*********
    <com.github.mikephil.charting.charts.PieChart
        android:layout_width="350dp"
        android:layout_centerInParent="true"
        android:layout_height="350dp"
        android:id="@+id/pieChartMaths"/>
        
Dpendencie:  
*************
     implementation 'com.github.PhilJay:MPAndroidChart:v3.1.0'        

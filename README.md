//# Widgets
Fluter 
Fluter me her cheez widget hoti ha
Run app 
Ak building function ha, jo ak widget ly ga
Esy jo b widget mely ga usy paint / draw kr dy ga
It accepts  a root-widget and draw/paint on the screen
My base code is a root-widget (ye code khu bnaya live tamplet)
Widget (/ component, part of screen/ section)
Widget ak class ka name ha
Her property  ky against ak widget ho ga

Youtube play list for widget
Firebase analystics (package of the week)
MaterialApp
Ak widget ka name ha is me pori applicate creat ho gi
Scaffold 	
Important widget ( her screen me design is sy hi banta ha)
AppBar
Use for app bar, top bar, bottom bar
Material 
Is sy app ka desgine banta ha
Style 
TextStyle 
Use for text style font size, font style
Centre 
Text ko center me  lana
child: Center(child: Text("KHADIM HUSSAIN"),),

Container (ye box hota)
40 sy zayda margin or pedding ni deni
child: Container(
  width: 400,
  height: 400,
  color: Colors.yellow,
margin: EdgeInsets.all(80), (4 tarf sy samae margin)
margin:EdgeInsets.only(left: 2,right: 4,bottom: 8, top:4), (specific margin)
margin:EdgeInsets.fromLTRB(2, 2,3,4),(apni marzi sy LTRB  margin dena)
margin:EdgeInsets.zero, (ZERO MARGIN DENA)
margin:EdgeInsets.symmetric(vertical: 20,horizontal: 30),ver or hor margin dena
padding: EdgeInsets.only(left: 4,right: 4,top: 4,bottom: 5),
(same as margin)
Decoration
In container widget Color property doesnot work outside the decoration
import 'package:flutter/material.dart';
void main() {
  runApp(
    MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text("Functions"),
        ),
        body: Material(
          child: Center(
            child: Container( //box
              width: 200, //box width
              height: 200,
              margin:EdgeInsets.symmetric(vertical: 20,horizontal: 20), //box margin
              padding: EdgeInsets.only(left: 4,right: 4,top: 4,bottom: 5), //box paddin
              decoration: BoxDecoration( // container ki decoration
                  color: Colors.yellow, //color dena
                  shape: BoxShape.rectangle, // box ki shap
                  gradient:LinearGradient( // gradien line mem dena
                    begin: Alignment.center, // gradien start point
                    end: Alignment.bottomLeft, // end point
                    stops: [0.50,0,1], // stop me % color fully green ya red ho ga
                    colors: [Colors.green, Colors.red, Colors.grey],// color range
                  ),
                  //border: Border.all(width:13, color: Colors.black, style: BorderStyle.solid), // 4 trf ak hi tara ka  border  lagana
                  //border: Border.symmetric(vertical: BorderSide(width: 12,color: Colors.brown), horizontal: BorderSide(width: 11, color: Colors.black)),// apn marzi sy border banana
                  //borderRadius: BorderRadius.all(Radius.elliptical(10, 10)) // box ko round krna apni marzi sy
                  borderRadius: BorderRadius.only(topRight: Radius.elliptical(10, 20), topLeft: Radius.elliptical(10, 20))

              ),



            ),
          ),
        ),
      ),
    ),
  );

}








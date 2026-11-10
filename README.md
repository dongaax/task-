
import 'package:flutter/material.dart';

void main(){
    
    runApp(MyApp());
}
class MyApp extends StatelessWidget{
  @override
  Widget build(BuildContext context) {

    return MaterialApp(
      home: Third_screen(),
    );
    
  }
  

}
class Fisrt_screen1 extends StatelessWidget{
  @override
  Widget build(BuildContext context) {
       return Scaffold(
        appBar: AppBar(
          leading: Icon(Icons.menu,color:Colors.white ,),
          centerTitle: true,
          title: Text("My Shop",style: TextStyle(color:Colors.white),),
           backgroundColor: Colors.indigo,
           actions: [
          Icon( Icons.shopping_cart,color: Colors.white,),
          Icon(Icons.notifications,color: Colors.white),
        ],
      ),

       body:Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Center(child: Text("Welcome Back!",style: TextStyle(color:Colors.black,
          fontSize: 32,fontWeight: FontWeight.bold ),),),
           Text("find the best prouduct of you",style: TextStyle(color: Colors.grey[700],fontSize: 18),
           ),
           
ElevatedButton(
  style: ElevatedButton.styleFrom(
    backgroundColor: Colors.indigo,
    foregroundColor: Colors.white,
    minimumSize: Size(280, 55),
    shape: StadiumBorder(),
  ),
  onPressed: () {},
  child: Text("Shop Now", style: TextStyle(fontSize: 18)),
),

SizedBox(height: 16),


OutlinedButton(
  style: OutlinedButton.styleFrom(
    foregroundColor: Colors.indigo,
    minimumSize: Size(280, 55),
    shape: StadiumBorder(),
  ),
  onPressed: () {},
  child: Text("View Offers", style: TextStyle(fontSize: 18)),
),
SizedBox(height: 16),


TextButton(
  onPressed: () {},
  child: Text("Skip", style: TextStyle(color: Colors.indigo, fontSize: 18)),
),
          
        ],
       ),
       bottomNavigationBar:BottomNavigationBar(items:[
            BottomNavigationBarItem(icon:Icon(Icons.home),label:"home") ,
             BottomNavigationBarItem(icon:Icon(Icons.search),label:"search") ,
            BottomNavigationBarItem(icon:Icon(Icons.person),label:"profile") ,
       ],
       ),


        );
      

  }


}
class Second_screen extends StatelessWidget{
  @override
  Widget build(BuildContext context) {
     return Scaffold(
         appBar: AppBar(
          leading: Icon(Icons.arrow_back),
          title: Text("Settings"),
          actions: [
            Icon(Icons.more_vert,color: Colors.black,)
          ],
         ),
         body: Center(
  child: Column(
    mainAxisAlignment: MainAxisAlignment.center,
    children: [
      Text(
        "Do you want to save changes?",
        style: TextStyle(
          fontSize: 22,
          fontWeight: FontWeight.bold,
        ),
      ),
      SizedBox(height: 30),
      Row(
        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
        children: [
          TextButton(
            onPressed: () {},
            child: Text(
              "Later",
              style: TextStyle(color: Colors.indigo, fontSize: 18),
            ),
          ),
          OutlinedButton(
            onPressed: () {},
            style: OutlinedButton.styleFrom(
              foregroundColor: Colors.indigo,
              shape: StadiumBorder(),
              minimumSize: Size(100, 50),
            ),
            child: Text("Cancel", style: TextStyle(fontSize: 18)),
          ),
          ElevatedButton(
            onPressed: () {},
            style: ElevatedButton.styleFrom(
              backgroundColor: Colors.indigo,
              foregroundColor: Colors.white,
              shape: StadiumBorder(),
              minimumSize: Size(100, 50),
            ),
            child: Text("Save", style: TextStyle(fontSize: 18)),
          ),
        ],
      ),
    ],
  ),
),
      bottomNavigationBar: BottomNavigationBar(
        items: [
          BottomNavigationBarItem(icon: Icon(Icons.home), label: "home"),
          BottomNavigationBarItem(icon: Icon(Icons.search), label: "search"),
          BottomNavigationBarItem(icon: Icon(Icons.person), label: "profile"),
        ],
      ),
    );
  }
}

class Third_screen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Colors.indigo[900],
        toolbarHeight: 80,
        leading: Padding(
          padding: EdgeInsets.all(12),
          child: CircleAvatar(
            backgroundColor: Colors.indigo[100],
            child: Text("A", style: TextStyle(color: Colors.indigo[900], fontWeight: FontWeight.bold)),
          ),
        ),
        title: Column(
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [
            Text("Ahmed Ali", style: TextStyle(color: Colors.white, fontSize: 22, fontWeight: FontWeight.bold)),
            Text("Online", style: TextStyle(color: Colors.white70, fontSize: 16)),
          ],
        ),
        actions: [
          Icon(Icons.phone, color: Colors.white),
          SizedBox(width: 20),
          Icon(Icons.videocam, color: Colors.white),
          SizedBox(width: 20),
        ],
      ),

      body: Row(
        children: [
          Expanded(
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Text("120", style: TextStyle(fontSize: 40, fontWeight: FontWeight.bold)),
                Text("Followers", style: TextStyle(fontSize: 20, color: Colors.grey)),
                SizedBox(height: 20),
                ElevatedButton(
                  onPressed: () {},
                  style: ElevatedButton.styleFrom(
                    backgroundColor: Colors.indigo,
                    foregroundColor: Colors.white,
                    shape: StadiumBorder(),
                    minimumSize: Size(140, 50),
                  ),
                  child: Text("Follow", style: TextStyle(fontSize: 18)),
                ),
              ],
            ),
          ),
          Expanded(
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Text("80", style: TextStyle(fontSize: 40, fontWeight: FontWeight.bold)),
                Text("Following", style: TextStyle(fontSize: 20, color: Colors.grey)),
                SizedBox(height: 20),
                OutlinedButton(
                  onPressed: () {},
                  style: OutlinedButton.styleFrom(
                    foregroundColor: Colors.indigo,
                    shape: StadiumBorder(),
                    minimumSize: Size(140, 50),
                  ),
                  child: Text("Message", style: TextStyle(fontSize: 18)),
                ),
              ],
            ),
          ),
        ],
      ),

      bottomNavigationBar: BottomNavigationBar(
        currentIndex: 0,
        selectedItemColor: Colors.indigo,
        items: [
          BottomNavigationBarItem(icon: Icon(Icons.home), label: "Home"),
          BottomNavigationBarItem(icon: Icon(Icons.search), label: "Search"),
          BottomNavigationBarItem(icon: Icon(Icons.person), label: "Profile"),
        ],
      ),
    );
  }
}


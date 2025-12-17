Setup

Step 1
Go To https://console.firebase.google.com/u/0/

Step 2 
Create A New Project Without Analytics Or Gemini. I Reccomend Naming It Something Like "Chat"

Step 3
After You Have Completed The Setup Process, Find The Build Section In Your Project

Step 4
Find The Authentication Section And Enable Auth With The Signup Method Of Email/Password

Step 5
Make Sure That Under Auth > Settings > User Actions  That Enable User Create is ENABLED

Step 6
Under The Build Section Find The Relatime Database Section And Enable A Realtime Database

Step 7
Under The Rules Section Of Your Realtime Database, Paste The Contents Of Rules.txt In This Repo And Then Click Publish

Step 8
Under The Build Section, Find Hosting DO NOT CLICK APP HOSTING, Then Click The Get Started Button

Step 9
Click Next Twice And Then Click Continue To Console

Step 10
To The Right Of The Project Overview Button Located In The Top Left, Click The Settings Icon, Then The Project Settings Button

Step 11
Once You Have Clicked The Project Settings Button, Make Sure You Are In The General Tab

Step 12
Scroll To The Very Bottom And Look For The Section With Some Code In It

Step 13
Copy Everything In const firebaseConfig = {}
Example
const firebaseConfig = {
  apiKey: "your api key",
  authDomain: "your rtdb domain",
  databaseURL: "your db url",
  projectId: "your project id",
  storageBucket: "your storage bucket url",
  messagingSenderId: "your messaging sender id",
  appId: "your app id",
  measurementId: "your measurement id" (THIS IS OPTIONAL)
};

Step 14
Go To The firebase.js File And Replace The firebaseConfig With Yours

Step 15
Open The Url In A New Tab And Sign Up

Step 16
Go Back To The Realtime Database Page, Look Under The Data Tab And Look For The Users Section And Expand It

Step 17
Find Your Account And Expand The User Id Then Find The Profile Section And Expand It

Step 18
Next To Where It Says Profile, Click The + Icon And Type isOwner Then Press Tab, Then Type true


To Make An Admin Only Channel, Make A Channel Called Admin-Chat

To Make it So You And Any User Can Type, Go To The Admin Page And Click The Verify Button

To Make A User Co Owner (Create, Rename, Delete Channels, Edit & Delete Messages Sent By Non Owner, Tester And Head Admin Users, Verify Users, Delete Typing Data, Mute Users, Bypass Slowmode, Bypass Message Char Limit) Do The Same Thing That You Did For The Owner, Except For Their Account And Instead Of Typing isOwner, Type isCoOwner

To Make A User Head Admin (Delete Messages Sent By Non Owner, Tester, Co Owner And Head Admin Users,  Mute Users, Bypass Slowmode, Bypass Message Char Limit) Do The Same Thing That You Did For The Owner, Except For Their Account And Instead Of Typing isOwner, Type isHAdmin

To Make A User Admin (Delete Messages Sent By Non Owner, Tester, Co Owner, Head Admin, And Other Admin Users, Bypass Slowmode) Do The Same Thing That You Did For The Owner, Except For Their Account And Instead Of Typing isOwner, Type isAdmin

One More Role There Is Is The 100th User To Sign Up. This Role Can Be Given To A User By Setting mileStone To True In Their Profile.

Only Owners, Testers, And Co Owners Can Access The Admin Panel.

If A User Is Typing For A Very Long Time, If You Are One Of The Roles Above, You Can Go To The Admin Panel And Delete The Typing Data.
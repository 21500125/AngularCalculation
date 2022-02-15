# AngularCalculation

# Web Page for Mathematical Calculations using Angular

## AIM:
To design a dynamic website to perform mathematical calculations using Angular Framwork

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS in component.html file

### Step 3:

Write typescript to perform the calculations.

### Step 4:

Validate the layout in various browsers.

### Step 5:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

# PROGRAM :

## Index.html:
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Mathcalculations</title>
  <base href="/">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
<body>
  <app-root></app-root>
</body>
</html>

## Parallel.component.ts:
import { Component } from "@angular/core";

@Component({
    selector:'Parallelogram-Area',
    templateUrl:'./parallel.component.html'
})

export class ParallelogramComponent{
    breadth:number;
    height:number;
    area:number;
    constructor(){
        this.breadth = 0
        this.height = 0
        this.area = this.breadth*this.height;
    }

    onCalculatearea()
    {
        this.area = this.breadth*this.height;
    }
}

## Cuboid.component.ts:
import { Component } from "@angular/core";

@Component({
    selector:'Cuboid-Volume',
    templateUrl:'./cuboid.component.html'
})

export class CuboidComponent{
    clength:number;
    cbreadth:number;
    cheight:number;
    volume:number;
    constructor(){
        this.clength = 0;
        this.cbreadth = 0;
        this.cheight = 0;
        this.volume = this.clength*this.cbreadth*this.cheight;
    }
    onCalculateVolume()
    {
        this.volume = this.clength*this.cbreadth*this.cheight;
    }
}

## Cuboid.component.html:
<div>
    Length:<input type="text" [(ngModel)]="clength">Meters<br/>
    <br/>
    Height:<input type="text" [(ngModel)]="cheight">Meters<br/>
    <br/>
    Breadth:<input type="text" [(ngModel)]="cbreadth">Meters<br/>
    <br/>
    <input type = "button" (click)="onCalculateVolume()" value="Calculate Volume"><br/>
    <br/>
    Volume:<input type="text" readonly value="0" [value]="volume">Meter<sup>3</sup>
</div>

## App.module.ts:
import { NgModule } from '@angular/core';
import { FormsModule } from '@angular/forms';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
import { CuboidComponent } from './cuboid/cuboid.component';
import { ParallelogramComponent } from './parallelogram/parallel.component';


@NgModule({
  declarations: [
    AppComponent,ParallelogramComponent,CuboidComponent
  ],
  imports: [
    BrowserModule,FormsModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }

## App.component.html:
<style>
    *{
box-sizing: border-box;
font-family: Arial, Helvetica, sans-serif;
}

body{
background-color: rgb(226, 164, 207);
color: black;
}

.container{
text-align: center;
width: 1080px;
height: 730px;
margin-left: auto;
margin-right: auto;
margin-top: auto;
}

.content{
display: block;
width: 100%;
margin-left: auto;
margin-right: auto;
background-color: rgb(233, 202, 145);
margin-top: 25px;
min-height: 275px;
}

.content1{
display: block;
width: 100%;
margin-left: auto;
margin-right: auto;
background-color: rgb(233, 202, 145);
margin-top: 25px;
min-height: 300px;
}

h1{
color: rgb(0, 0, 0);
text-align: center;
padding-top: 20px;
}

h2{
color: rgb(0, 0, 0);
text-align: center;
padding-top: 20px;
}

.formelement{
text-align: center;
padding-top: 20px;
font-size: larger;
}


.footer{
display: inline-block;
width: 100%;
height: 35px;
background-color: darksalmon;
color: black;
text-align: center;
padding-top: 7px;
font-size: large;
}

</style>

<body>
    <div class="container">
    <h1>Math Calculations</h1>
    <div class="content">
        <h2><u>Area of Parallelogram</u></h2>
        <Parallelogram-Area class="formelement"></Parallelogram-Area>
    </div>
    <div class="content1">
        <h2><u>Volume of Cuboid</u></h2>
        <Cuboid-Volume class="formelement"></Cuboid-Volume>
    </div>
    <div class="footer">
        Developed by Vishranthi A
    </div>
    </div>

</body>


## OUTPUT:
![ZZ1](https://user-images.githubusercontent.com/94219582/154132685-b5c09793-6a19-44f1-b0c9-971409a91f01.PNG)
![ZZ2](https://user-images.githubusercontent.com/94219582/154132712-c3fa5141-2b60-418a-986c-7fc4939031e7.PNG)

## Result:
Thus a Mathmetical Calculation website is created using Angular.

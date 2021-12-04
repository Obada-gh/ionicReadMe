# intro To ionic:
![intro](images\introIonic.png)
![intro2](images\intro2.png)
![benAng](images\benfisofAng.png)

# install angular cli:
`npm install -g @angular/cli`

![installAngler](images\introIonic.png)

`ng --version` to check if it installed

to craete new angler project `ng new nameoftheproject`

to lunch the sever: `ng serve`

# Angluer structcher :

![angler](images\anglerSrc.png)
![bundels](images\bundels.png)

# Angluer Road To learn :
![roadAng](images\roadAng.png)
![roadAdv](images\roadAngAdv.png)

# TypeScript:

1. strong typing
2. oop
3. compile-time errors
4. great tooling

- only differnt is variable need to set the type for it.

Ts\\\\\\\\\\\\\\\\js\\\\\\\\\\\\\\\\\\Ts : Ts can take js
- browser can not understand the TS. we need to convert to js

- To use the TS run `npm install -g typescript`
- check ver `tsc --version`
- to convert : 
- ![convert](images\convert.png)
- you can till him its a string and you can see all method avelable there ![newFea](images\newFinTs.png)or use `(m as string)`
- note : ![and in terminal](images\andInTerminal.png)



```
interface Point{
    x:number,
    y:number
};

// interface for the data enter

let drawPoint = (point: Point) => {
    //....
};

drawPoint({
    x:1,
    y:2
});


```

```
void //do not return anything
```

- class is better

```
class Point {
    x: number;
    y: number:

    draw(){
        console.log('X:' + this.x + ', Y: ' + this.y)
    };

    getDistance(another: Point){
        //...
    }

}

let point = new Point();

point.x = 1;
point.y = 2;
point.draw();

```

![class](images\class.png)

![acsses](images\accsessModi.png)

if you use privete word in variable with class you will not acess it from the class

![class2](images\class2.png)

![usemodel](images\model.png)

- (import and export).

# Back to angular:
## componet:
The area that the user see
![componet](images\componet.png)
![componet2](images\componet2.png)

* To create componet:
1. create a component in app folder ex:`courses.compnent.ts` add code example:
```
import { Component } from "@angular/core";

@Component({
  selector: 'courses',
  template: '<h2>Courses</h2>'
})
export class CoursesComponent{


}
```
![compnetCode](images\componetEx.png)
2. register it in a module:
![regInModle](images\regInModel.png)
3. add an element in an html markup ex : `<courses></courses>`

4. you can finish all three steps above by `ng g c course`
![ezStep](images\ezSteps.png)

## Example of how to use Component :
```
import { Component } from "@angular/core";

@Component({
  selector: 'courses',
  template: `<h2>{{"Title: "+getTitle()}}</h2>
  <ul>
  <li *ngFor='let course of courses'>
  {{course}}
  </li>
  </ul>`
})
export class CoursesComponent{
  title = 'List of courses';
  getTitle(){
    return this.title;
  }

  courses=['1','2',3]

```
## modules:

group of componets.

## services:
1. ex create file in app folder ex`courses.service.ts`
and add your http service or like this example of code if you want: 
```
export class CoursesService {
  getCourses() {
    return ['1','2','3'];
  }
};


```
2. imported from the file and use the constructer like that in the component :

```
import { Component } from "@angular/core";
import { CoursesService } from "./path of the file";





@Component({
  selector: 'courses',
  template: `<h2>{{"Title: "+getTitle()}}</h2>
  <ul>
  <li *ngFor='let course of courses'>
  {{course}}
  </li>
  </ul>`
})
export class CoursesComponent{
  title = 'List of courses';
  getTitle(){
    return this.title;
  }

  courses = [1,2,3]

  constructor(service: CoursesService){
    this.courses = service.getCourses();
  }



}

```

3. if you want to do it fast `ng g s email` email is the name of the service

# Back to ionic 4 with maxmlean :

# intro:

1. install ionic `npm install -g ionic`
2. run `ionic start`
3. cd to your project
4. run `ionic serve`
5. ionic road ![ionicRoad](.\images\ioncRoad.png)


# core Building Blocks:

![ionicBuildingBlocks](.\images\ionicBuildingBlocks.png)

## components:

![ionicComponent](images\ionicComponents.png)
![ionicbutton](images\ionicbutton.png)

## lets dive into the project : 

![1](images\Screenshot_1.png)

1. you can work with ionic dirctly with html by cdn
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <script
      type="module"
      src="https://cdn.jsdelivr.net/npm/@ionic/core/dist/ionic/ionic.esm.js"
    ></script>
    <script
      nomodule
      src="https://cdn.jsdelivr.net/npm/@ionic/core/dist/ionic/ionic.js"
    ></script>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/@ionic/core/css/ionic.bundle.css"
    />
  </head>
  <body>
      <ion-app>
          <ion-header>
              <ion-toolbar color='primary'>
                  <ion-title>Budget Planner</ion-title>
              </ion-toolbar>
          </ion-header>
          <ion-card></ion-card>
          <ion-content>
              <ion-item><ion-label posittion='floating'>Expense Reason</ion-label>>
                <ion-input type=text></ion-input>
            </ion-item>
              

          </ion-content>
      </ion-app>
  </body>
</html>

```
2. core component types:
![2](images\Screenshot_2.png)
![2](images\Screenshot_2.png)
![2](images\Screenshot_3.png)
![2](images\Screenshot_4.png)
![2](images\Screenshot_5.png)
![2](images\Screenshot_6.png)
![2](images\Screenshot_7.png)


3. `ionic generate` To create anything in angluer

![2](images\Screenshot_8.png)
![2](images\Screenshot_9.png)



`ng build`

`ionic capacitor add android`
`ionic capacitor copy android`
`ionic capacitor run android`
`ionic capacitor run android -l`













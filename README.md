# data-and-code

import { Project } from "https://unpkg.com/leopard@^1/dist/index.esm.js";
 
import Stage from "./Stage/Stage.js";
import _1 from "./_1/_1.js";
import F from "./F/F.js";
import _2 from "./_2/_2.js";
import _3 from "./_3/_3.js";
import _4 from "./_4/_4.js";
import _5 from "./_5/_5.js";
import D from "./D/D.js";
import C from "./C/C.js";
import N from "./N/N.js";
import A from "./A/A.js";
import Sun from "./Sun/Sun.js";
import Sun2 from "./Sun2/Sun2.js";
import Sun3 from "./Sun3/Sun3.js";
import Stop from "./Stop/Stop.js";
import Stop2 from "./Stop2/Stop2.js";
 
const stage = new Stage({ costumeNumber: 1 });
 
const sprites = {
 _1: new _1({
   x: -182,
   y: -118,
   direction: 90,
   costumeNumber: 1,
   size: 30,
   visible: true,
   layerOrder: 6
 }),
 F: new F({
   x: -14,
   y: 17,
   direction: 90,
   costumeNumber: 1,
   size: 100,
   visible: true,
   layerOrder: 1
 }),
 _2: new _2({
   x: -137.47991131745343,
   y: 94.42627697710594,
   direction: 90,
   costumeNumber: 1,
   size: 30,
   visible: true,
   layerOrder: 3
 }),
 _3: new _3({
   x: -168.26735672756553,
   y: -36.17577844946945,
   direction: 90,
   costumeNumber: 1,
   size: 30,
   visible: true,
   layerOrder: 2
 }),
 _4: new _4({
   x: -166.98095567841239,
   y: -83.78957843008942,
   direction: 90,
   costumeNumber: 1,
   size: 30,
   visible: true,
   layerOrder: 5
 }),
 _5: new _5({
   x: -125.85921955829158,
   y: 124.45281778920699,
   direction: 90,
   costumeNumber: 1,
   size: 30,
   visible: true,
   layerOrder: 4
 }),
 D: new D({
   x: 10,
   y: -6,
   direction: 90,
   costumeNumber: 1,
   size: 100,
   visible: false,
   layerOrder: 7
 }),
 C: new C({
   x: 5,
   y: 19,
   direction: 90,
   costumeNumber: 1,
   size: 100,
   visible: false,
   layerOrder: 8
 }),
 N: new N({
   x: 13,
   y: 79,
   direction: 90,
   costumeNumber: 1,
   size: 100,
   visible: false,
   layerOrder: 9
 }),
 A: new A({
   x: 88,
   y: 39,
   direction: 90,
   costumeNumber: 1,
   size: 100,
   visible: false,
   layerOrder: 10
 }),
 Sun: new Sun({
   x: 175,
   y: 119,
   direction: 60,
   costumeNumber: 1,
   size: 100,
   visible: true,
   layerOrder: 15
 }),
 Sun2: new Sun2({
   x: 181.18145188192668,
   y: 118.70879569808017,
   direction: -150,
   costumeNumber: 1,
   size: 100,
   visible: false,
   layerOrder: 11
 }),
 Sun3: new Sun3({
   x: -22.990786856244256,
   y: -154.55487561028536,
   direction: 60,
   costumeNumber: 1,
   size: 100,
   visible: false,
   layerOrder: 12
 }),
 Stop: new Stop({
   x: -77,
   y: -110,
   direction: 60,
   costumeNumber: 1,
   size: 100,
   visible: false,
   layerOrder: 14
 }),
 Stop2: new Stop2({
   x: 188.81607747061864,
   y: 126.22644108423037,
   direction: -150,
   costumeNumber: 1,
   size: 100,
   visible: false,
   layerOrder: 13
 })
};
 
const project = new Project(stage, sprites, {
 frameRate: 30 // Set to 60 to make your project run faster
});
export default project;
 
 
 
Code for Avalon data
 
/* eslint-disable require-yield, eqeqeq */
 
import {
 Sprite,
 Trigger,
 Watcher,
 Costume,
 Color,
 Sound
} from "https://unpkg.com/leopard@^1/dist/index.esm.js";
 
export default class A extends Sprite {
 constructor(...args) {
   super(...args);
 
   this.costumes = [
     new Costume(
       "Screen Shot 2022-10-31 at 3",
       "./A/costumes/Screen Shot 2022-10-31 at 3.png",
       { x: 480, y: 267 }
     )
   ];
 
   this.sounds = [];
 
   this.triggers = [
     new Trigger(Trigger.GREEN_FLAG, this.whenGreenFlagClicked),
     new Trigger(Trigger.KEY_PRESSED, { key: "a" }, this.whenKeyAPressed),
     new Trigger(
       Trigger.KEY_PRESSED,
       { key: "space" },
       this.whenKeySpacePressed
     )
   ];
 }
 
 *whenGreenFlagClicked() {
   this.visible = false;
 }
 
 *whenKeyAPressed() {
   this.visible = true;
 }
 
 *whenKeySpacePressed() {
   this.visible = false;
 }
}
 
 
Code for Collaroy data
 
/* eslint-disable require-yield, eqeqeq */
 
import {
 Sprite,
 Trigger,
 Watcher,
 Costume,
 Color,
 Sound
} from "https://unpkg.com/leopard@^1/dist/index.esm.js";
 
export default class C extends Sprite {
 constructor(...args) {
   super(...args);
 
   this.costumes = [
     new Costume(
       "Screen Shot 2022-10-31 at 3",
       "./C/costumes/Screen Shot 2022-10-31 at 3.png",
       { x: 257, y: 141 }
     )
   ];
 
   this.sounds = [];
 
   this.triggers = [
     new Trigger(Trigger.GREEN_FLAG, this.whenGreenFlagClicked),
     new Trigger(
       Trigger.KEY_PRESSED,
       { key: "space" },
       this.whenKeySpacePressed
     ),
     new Trigger(Trigger.KEY_PRESSED, { key: "c" }, this.whenKeyCPressed)
   ];
 }
 
 *whenGreenFlagClicked() {
   this.visible = false;
 }
 
 *whenKeySpacePressed() {
   this.visible = false;
 }
 
 *whenKeyCPressed() {
   this.visible = true;
 }
}
 
 
 
Code for Dee Why data
 
/* eslint-disable require-yield, eqeqeq */
 
import {
 Sprite,
 Trigger,
 Watcher,
 Costume,
 Color,
 Sound
} from "https://unpkg.com/leopard@^1/dist/index.esm.js";
 
export default class D extends Sprite {
 constructor(...args) {
   super(...args);
 
   this.costumes = [
     new Costume(
       "Screen Shot 2022-10-31 at 3",
       "./D/costumes/Screen Shot 2022-10-31 at 3.png",
       { x: 274, y: 154 }
     )
   ];
 
   this.sounds = [];
 
   this.triggers = [
     new Trigger(Trigger.GREEN_FLAG, this.whenGreenFlagClicked),
     new Trigger(Trigger.KEY_PRESSED, { key: "d" }, this.whenKeyDPressed),
     new Trigger(
       Trigger.KEY_PRESSED,
       { key: "space" },
       this.whenKeySpacePressed
     )
   ];
 }
 
 *whenGreenFlagClicked() {
   this.visible = false;
 }
 
 *whenKeyDPressed() {
   this.visible = true;
 }
 
 *whenKeySpacePressed() {
   this.visible = false;
 }
}
 
 
Code for Freshwater Data
 
/* eslint-disable require-yield, eqeqeq */
 
import {
 Sprite,
 Trigger,
 Watcher,
 Costume,
 Color,
 Sound
} from "https://unpkg.com/leopard@^1/dist/index.esm.js";
 
export default class F extends Sprite {
 constructor(...args) {
   super(...args);
 
   this.costumes = [
     new Costume(
       "Screen Shot 2022-10-31 at 2",
       "./F/costumes/Screen Shot 2022-10-31 at 2.png",
       { x: 222, y: 345 }
     )
   ];
 
   this.sounds = [];
 
   this.triggers = [
     new Trigger(Trigger.GREEN_FLAG, this.whenGreenFlagClicked),
     new Trigger(Trigger.KEY_PRESSED, { key: "f" }, this.whenKeyFPressed),
     new Trigger(
       Trigger.KEY_PRESSED,
       { key: "space" },
       this.whenKeySpacePressed
     )
   ];
 
   this.vars.whenThisSpriteIsClicked2 = 0;
 }
 
 *whenGreenFlagClicked() {
   this.visible = false;
 }
 
 *whenKeyFPressed() {
   this.visible = true;
 }
 
 *whenKeySpacePressed() {
   this.visible = false;
 }
}
 
 
Code for Newport Data
 
/* eslint-disable require-yield, eqeqeq */
 
import {
 Sprite,
 Trigger,
 Watcher,
 Costume,
 Color,
 Sound
} from "https://unpkg.com/leopard@^1/dist/index.esm.js";
 
export default class N extends Sprite {
 constructor(...args) {
   super(...args);
 
   this.costumes = [
     new Costume(
       "Screen Shot 2022-10-31 at 3",
       "./N/costumes/Screen Shot 2022-10-31 at 3.png",
       { x: 251, y: 273 }
     )
   ];
 
   this.sounds = [];
 
   this.triggers = [
     new Trigger(Trigger.GREEN_FLAG, this.whenGreenFlagClicked),
     new Trigger(Trigger.KEY_PRESSED, { key: "n" }, this.whenKeyNPressed),
     new Trigger(
       Trigger.KEY_PRESSED,
       { key: "space" },
       this.whenKeySpacePressed
     )
   ];
 }
 
 *whenGreenFlagClicked() {
   this.visible = false;
 }
 
 *whenKeyNPressed() {
   this.visible = true;
 }
 
 *whenKeySpacePressed() {
   this.visible = false;
 }
}

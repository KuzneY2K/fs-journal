# MVC

export class Gachamon {
    constructor (name, icon, picture){
        this.name = name
        this.icon = icon
        this.picture = picture
    }
}

let newmon = new Gachamon('New Mon', imglink, imgfile)

constructors can share names with parameter names



router

import {controller name} from './ file path'

export const router = [{
    path: '',
    controller: [controller name],
    view: html goes here
}]

drawGachamonList(){
    const gachamon = AppState.gachamons

    gachamon.forEach(g => g.ListTemplater)
}



gotta be paired with .on
Adds a listener/observer on change and then does function
AppState.on('activeGachamon', this.drawActiveGachamon)
```js
class Matchup {
    constructor(overrides = {}) {
        const types = [
            "normal", "fighting", "flying", "poison", "ground", "rock", "bug", "ghost", "steel",
            "fire", "water", "grass", "electric", "psychic", "ice", "dragon", "dark", "fairy"
        ]
        
        type.forEach(t => this[t] = 1);
    }
    
    Object.assign(this, overrides);
}

const waterMU = new Matchup({grass: 2, electric: 2, steel: .5, fire: .5, water: .5, ice: .5})

// water = {
//     normal: 1,
//     fighting: 1,
//     flying: 1,
//     poison: 1,
//     ground: 1,
//     rock: 1,
//     bug: 1,
//     ghost: 1,
//     steel: .5,
//     fire: .5,
//     water: .5,
//     grass: 2,
//     electric: 2,
//     psychic: 1,
//     ice: .5,
//     dragon: 1,
//     dark: 1,
//     fairy: 1
// }

const groundMU = new Matchup({water: 2, grass: 2, ice: 2, poison: .5, rock: .5, electric: 0})

// ground = {
//   normal: 1,
//   fighting: 1,
//   flying: 1,
//   poison: .5,
//   ground: 1,
//   rock: .5, 
//   bug: 1,
//   ghost: 1,
//   steel: 1,
//   fire: 1,
//   water: 2,
//   grass: 2,
//   electric: 0,
//   psychic: 1,
//   ice: 2,
//   dragon: 1,
//   dark: 1,
//   fairy: 1
// }

const waterGroundMU = dualType(waterMU, groundMU)

// waterGroundMU = {
//     normal: 1,
//     fighting: 1,
//     flying: 1,
//     poison: .5,
//     ground: 1,
//     rock: .5,
//     bug: 1,
//     ghost: 1,
//     steel: .5,
//     fire: .5,
//     water: 1,
//     grass: 4,
//     electric: 0,
//     psychic: 1,
//     ice: 1,
//     dragon: 1,
//     dark: 1,
//     fairy: 1
// }
```

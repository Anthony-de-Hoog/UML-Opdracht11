# UML-Opdracht11

## Opdracht A
Een UML componentendiagram wordt gebruikt om de hoge niveaustructuur van een softwaresysteem weer te geven. Het focust op de fysieke componenten van een systeem, zoals modules, bibliotheken, bestanden, en interfaces, en hoe deze met elkaar samenwerken. Het is handig in de ontwerpfase om de softwarearchitectuur te definiëren.![Screenshot 2025-01-16 193401](https://github.com/user-attachments/assets/6c8844d8-2e07-400f-9d53-8ebc93bfb671)


## Opdracht B
```mermaid




classDiagram

class DamageSystem{
    - int damage
    +  DamageTarget()
}

class TriggerDamageScript{
    - bool damageModeActive
    + AddAlly()
    + AddEnemy()
    + EnableDamageMode()
    + ResetMouseClick()
    + DisableAllMouseClicks()
    + SwitchTurn()
    + OnDestroy()
}

class HPSystem{
    + float hp
    + Die()
}

class CrusaderHealth{
    + float hp
}

class HighwayManHealth{
    + float hp     
}

class PlagueDoctorHP{
    + float hp
}

class VestalHealth{
    + float hp
}

class Acolyte{
    + float hp
}

class RabbleHealth{
    + float hp
}

class SoldierHealth{
    + float hp
}

class HealthBar{
    + GoAway()
}

class CrusaderBar{
    + UpdateHealthBar()
}

class CultistBar{
    + UpdateHealthBar()
}

class HighwayBar{
    + UpdateHealthBar()
}

class PlagueDrBar{
    + UpdateHealthBar()
}

class RubbleBar{
    + UpdateHealthBar()
}

class SoldierBar{
    + UpdateHealthBar()
}

class VestalBar{
    + UpdateHealthBar()
}

class MouseClick{
    - enum myState
}

class EndButtons{
    + Restart()   
    - Quit()
}

class EndText{
    - Text
}

class BattleSystem{ 
    - Action NextTurn
    + BattleStateSwitch()
    + IsAlliesDefeated()
    + IsEnemiesDefeated()
    + DelayAndSwitchState()
    + GetNextValidUnvisitedState()
    + IsStateValid()
    + SpawnPrefabs()
    + HighlightTurn()
    + EnemyAttack()
    + GetRandomAlly()
}

HPSystem <-- CrusaderHealth
HPSystem <-- HighwayManHealth
HPSystem <-- PlagueDoctorHP
HPSystem <-- VestalHealth
HPSystem <-- Acolyte
HPSystem <-- RabbleHealth
HPSystem <-- SoldierHealth

HealthBar <-- CrusaderBar
HealthBar <-- CultistBar
HealthBar <-- HighwayBar
HealthBar <-- PlagueDrBar
HealthBar <-- VestalBar
HealthBar <-- RubbleBar
HealthBar <-- SoldierBar

HPSystem <.. DamageSystem

MouseClick <.. TriggerDamageScript
BattleSystem <.. TriggerDamageScript

BattleSystem <.. HealthBar
DamageSystem <.. MouseClick

TriggerDamageScript <.. BattleSystem
EndText <.. BattleSystem
EndButtons <.. BattleSystem



```

# *Lab04*

ในเกม RPG นี้ จะมีสายอาชีพ ซึ่งแต่ละสายจะมีค่าสถานะที่แตกต่างกัน

## สายอาชีพ
- ใช้ `String applyJob()` เพื่อตั้งค่าอาชีพของตัวละคร
### *Warrior*
สายสมดุล มีพลังโจมตีและพลังชีวิตปานกลาง

| **Stat** |     |
|----------|-----|
| ATK      | 10  |
| HP       | 100 |
| DEF     | 5 |


### *Tank*
สายป้องกัน มีพลังชีวิตสูงมาก แต่สร้างความเสียหายได้น้อย

| **Stat** |     |
|----------|-----|
| ATK      | 5  |
| HP       | 200 |
| DEF     | 8 |

- สร้าง `public int setHpTank()` เพื่อ set ค่าพลังชีวิตของตัวละครสาย Tank
- สร้าง `public int setAttackTank()` เพื่อ set ค่าพลังชีวิตของตัวละครสาย Tank

### *Assassin*
สายโจมตี มีพลังโจมตีสูงมาก แต่มีพลังชีวิตที่น้อย

| **Stat** |     |
|----------|-----|
| ATK      | 20  |
| HP       | 50 |
| DEF     | 0 |

- สร้าง `public int setHpAssassin()` เพื่อ set ค่าพลังชีวิตของตัวละครสาย Assassin
- สร้าง `public int setAttackAssassin()` เพื่อ set ค่าพลังชีวิตของตัวละครสาย Assassin


## ของสวมใส่
- สร้าง class Equipment เพื่อเก็บอุปกรณ์สวมใส่ต่าง ๆ
  - Variable
    - `private int gauntletLevel;`
    - `private int ringLevel;`
    - `private int bootsLevel;`
    - `private int defense;`
    - `private int attack;`
    - `private int hp;`
  - Operation
    - `int getDefense()`
    - `int getAttack()`
    - `int getHp()`

มีของสวมใส่ 3 ชนิด
### *Gauntlet*
+Atk

    public void gauntletLevelUp() {
        gauntletLevel++;
        attack *=(1+0.05*level);
    }

    public int getGauntletLevel() {
        return gauntletLevel;
    }

### *Ring*
+defense

    public void ringLevelUp() {
        ringLevel++;
        defense *=(1+0.05*level);
    }
    public int getRingLevel() {
        return ringLevel;
    }

### *Boots*
+Hp

    public void bootsLevelUp() {
        bootsLevel++;
        hp *=(1+0.05*level);
    }
    public int getBootsLevel() {
        return bootsLevel;
    }

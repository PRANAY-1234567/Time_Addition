# ⏰ Time Addition Using Python Class (OOP)

## 📌 Description

This Python program demonstrates **Object-Oriented Programming (OOP)** by creating a `Time` class. It allows you to store time in hours, minutes, and seconds, and perform **addition of two time objects** with proper handling of overflow (seconds → minutes, minutes → hours).

---

## 🚀 Features

* Defines a `Time` class with hours, minutes, and seconds
* Uses constructor with default values
* Displays time in formatted `HH : MM : SS` format
* Adds two time objects with proper carry handling

---

## 🛠️ How It Works

1. A class `Time` is created with:

   * `hrs`, `min`, `sec` as attributes
2. The `display()` method prints time in **2-digit format**
3. The `addition()` method:

   * Adds seconds and converts extra seconds into minutes
   * Adds minutes and converts extra minutes into hours
   * Adds hours to get the final result
4. Three objects are used:

   * `t1` → First time
   * `t2` → Second time
   * `t3` → Result of addition

---

## 💻 Code

```python id="xk92sd"
class Time:
    def __init__(self, hrs=0, min=0, sec=0):
        self.hrs = hrs
        self.min = min
        self.sec = sec

    def display(self):
        print(f"{self.hrs:02d} : {self.min:02d} : {self.sec:02d}")

    def addition(self, x):
        r = Time()

        # Add seconds
        r.sec = self.sec + x.sec
        r.min = r.sec // 60
        r.sec = r.sec % 60

        # Add minutes
        r.min = r.min + self.min + x.min
        r.hrs = r.min // 60
        r.min = r.min % 60

        # Add hours
        r.hrs = r.hrs + self.hrs + x.hrs

        return r

t1 = Time(10, 25, 45)
t2 = Time(9, 38, 30)

t3 = t1.addition(t2)

t1.display()
t2.display()
t3.display()
```

---

## ▶️ Example Output

```id="y2md9a"
10 : 25 : 45
09 : 38 : 30
20 : 04 : 15
```

---

## 📚 Concepts Used

* Class and Object
* Constructor with default values
* Method creation
* Arithmetic operations
* Carry handling logic (like real clock addition)

---

## 🎯 Use Case

This program helps beginners understand:

* How real-world problems (like time calculation) are solved using OOP
* How to manage overflow conditions logically

---

## 🔧 Future Improvements

* Add subtraction of time
* Accept user input instead of hardcoded values
* Convert time into total seconds and vice versa
* Add validation (e.g., seconds < 60, minutes < 60)

----

## 📄 License

This project is open-source and free to use.

<img width="768" height="788" alt="image" src="https://github.com/user-attachments/assets/4feadd4c-24ab-4126-a311-1540a9ba41c6" />

# Predavanja sa matematike 1

Matematika 1: 
- Skupovi brojeva, operacije nad skupovima, relacije, linearna i kvadratna funkcija...

[Predavanje 03.10.2023]()

- Kompleksni brojevi, algebarski, geometrijski, trigonometrijski oblik (dokazi + linkovi)

[Predavanje 04.10.2023]()

- Vežbe, kvadratna funkcija, kvadratne jednačine i nejednačine, apsolutne vrednosti:
> U linkovima ispod predavanja stoje izvodjenja ekstremnih vrenosti f-ja, za rešenja zadataka javiti se u DM

[Vežbe 05.10.2023]()

KLIKNUTI link, on renderuje animaciju!!

[ANIMACIJA](https://github.com/swagineering/swagineering.github.io/assets/142833312/ddfc3191-57a7-4675-9921-f63ecef36bc4)

### Python kod za datu animaciju. Prva funkcija je f(x) = (x-3) ^ 2, a druga f(x) = x ^ 2. Oduzimanje neke konstante A od x, pomera grafuk u desno!

```
from manim import *

class image_one(Scene):
    def construct(self):
        ax = Axes(
            x_range=[-2, 7, 1], #domen
            y_range=[-2 ,7 ,1], #kodomen
            tips = False,
            axis_config={"include_numbers": True},
        )

        text1 = Text("x").set_color(BLUE)
        text2 = Text("f(x)").set_color(RED)

        labels = ax.get_axis_labels(
            text1, text2
        )

        self.add(ax)
        self.play(Write(labels))

        #definisanje funkcije
        quadfunc1 = ax.plot(
            lambda x : x ** 2
        )

        quadfunc2 = ax.plot(
            lambda x : (x-3) ** 2
        )
        
        self.play(Create(quadfunc2))
        self.play(FadeOut(quadfunc2))
        self.play(Create(quadfunc1))
        self.play(FadeOut(quadfunc1))
        self.wait(2)
```



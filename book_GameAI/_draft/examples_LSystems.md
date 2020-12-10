
# L-Systems
examples to be used in 
http://www.malsys.cz/Process

## HilbertCurve
```
lsystem HilbertCurve {
 set compressSvg = false;
  set symbols axiom = L;
  set iterations = 2;
 
  interpret F as DrawForward(8);
  interpret + as TurnLeft(90);
  interpret - as TurnLeft(-90);
 
  rewrite L to + R F - L F L - F R +;
  rewrite R to - L F + R F R + F L -;
}
 
process all with SvgRenderer;
```

## Koch CUrve
```
lsystem KochCurve {
  set compressSvg = false;
  set symbols axiom = F; // F - - F - - F;
  set iterations = 1;
 
  // normalize line length to have (result image will have always same size)
  interpret F as DrawForward(2 ^ -(currentIteration * 3 / 2) * 512);
  interpret + as TurnLeft(60);
  interpret - as TurnLeft(-60);
 
  rewrite F to F + F - - F + F;
}
 
process all with SvgRenderer;
```

## plant
```
lsystem Plant3 {
 
  set symbols axiom = F(0);
  set initialAngle = 90;
  set iterations = 1;
  set randomSeed = 0;
  set compressSvg = false;
 
  interpret F(x) as DrawForward(12, 1+x*2,
    darken(#00FF00, random(0 + 0.1*x, 0.3 + 0.05*x)));
  interpret + as TurnLeft(22 + random(-5, 5));
  interpret - as TurnLeft(-22 + random(-5, 5));
  interpret [ as StartBranch;
  interpret ] as EndBranch;
 
  rewrite F(x) to F(x+1) F(x+1) - [ - F(0) + F(0) + F(0) ] + [ + F(0) - F(0) - F(0) ];
}
 
process all with SvgRenderer;
```

## MengerSponge 3D
```
lsystem MengerSponge {
 
  set iterations = 3;
  set symbols axiom = F;
 
  interpret F as DrawForward(10, 10, #FFFFFF);
  interpret f as MoveForward(5);
  interpret + as Yaw(90);
  interpret - as Yaw(-90);
  interpret ^ as Pitch(90);
  interpret & as Pitch(-90);
 
  rewrite F to
    - f f + & f f ^ F F F +f+f- F F +f+f- F F +f+f- F
    -f+f+f^f F F &f&f^ F F &f&f^ F ^ ^ f f f & + f F F &f&f^ F
    ^ ^ f f f & + f F F &f&f^ F ^ ^ f f f & + f F f & f f ^ +
    + f f - f f f f f;
  rewrite f to f f f;
}
 
process all with ThreeJsRenderer;
```

## Sierpinski Trangle
```
lsystem SierpinskiTrangle {
  set compressSvg = false;
  set symbols axiom = F + F + F;
  set iterations = 7;
 
  interpret F f as MoveForward(2 ^ -currentIteration * 600);
  interpret + as TurnLeft(120);
  interpret - as TurnLeft(-120);
  interpret < as StartPolygon(0, 0);
  interpret . as RecordPolygonVertex;
  interpret > as EndPolygon;
 
  rewrite F to < . F . + F . > + f + f F;
  rewrite f to f f;
  rewrite < to nothing;
  rewrite . to nothing;
  rewrite > to nothing;
}
 
process all with SvgRenderer;
```

## GosperCurve Ascii
```
lsystem AsciiHexaGosperCurve {
 
  set symbols axiom = L;
  set iterations = 3;
  set scale = 2;
 
  rewrite L to L + R + + R - L - - L L - R +;
  rewrite R to - L + R R + + R + L - - L - R;
 
  interpret R L as DrawLine;
  interpret + as TurnLeft;
  interpret - as TurnRight;
}
 
process all with HexAsciiRenderer;
```

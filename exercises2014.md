
## AIAD Exercises - 2013 / 2014

**1.**

### Beliefs

- Current altitude
- Current speed
- Current course
- Maximum and minimum altitude limits
- Existence of intense fog
- Existence of air pockets
- Existence of other airplanes
- Wind speed

### Desires

- Reach destination safely
- Reach destination in the shortest possible time

### Intentions

- Avoid collision with other airplanes
- Avoid exceeding altitude limits
- Avoid strong fog
- Avoid air pockets
- Escape or safely traverse through strong winds
- Reach the destination quickly

### Belief Revision Function

- Update current altitude, speed and route values, as well as altitude limits
- Use sensors to determine the presence of fog / air pockets / airplanes / strong winds

### Option Generation Function

- If no threats to airplane safety are detected and the airplane isn't currently attempting to avoid a threat, focus on reaching the destination quickly
- Otherwise, focus on reaching the destination safely

### Filter

- Prioritize safety critical intentions, especially avoiding collision with other planes

### Action Selection

- Avoid collision with other airplanes: change altitude / course
- Avoid exceeding altitude limits: increase / decrease altitude accordingly
- Avoid strong fog / air pockets: change altitude
- Escape or safely traverse through strong winds: reduce speed and / or change route
- Reach the destination quickly: calculate the shortest route to the destination and redirect the plane

**2. a)**

From low-level to high-level layers:

```
- Obstacle detected -> Change movement direction
- Carrying ore and in mothership -> Drop ore
- Full capacity -> Move towards mothership
- Low mothership signal -> Invert movement direction
- Ore detected -> Pick up ore
- Otherwise -> Move randomly
```

**b)**

```
- Obstacle detected -> Change movement direction
- Carrying ore and in mothership -> Drop ore
- Full capacity -> Move towards mothership
- Low mothership signal -> Invert movement direction
- Ore detected -> Pick up ore
- Radioactive trail detected -> Move along trail
- Otherwise -> Move randomly
```

**3. a)**

### I

```
Q(C, D) = 0 + 1.0 * (0 + 0.8 * 0 - 0) = 0
Q(D, B) = 0
Q(B, F) = 100
```

State / Action|A|B|C|D|E|F
-|-|-|-|-|-|-
A|❌|❌|❌|❌|0|❌
B|❌|❌|❌|0|❌|100
C|❌|❌|❌|0|❌|❌
D|❌|80|0|❌|0|❌
E|0|❌|❌|0|❌|0
F|❌|0|❌|❌|0|0

### II

```
Q(C, D) = 0
Q(D, E) = 0
Q(E, F) = 100
```

State / Action|A|B|C|D|E|F
-|-|-|-|-|-|-
A|❌|❌|❌|❌|0|❌
B|❌|❌|❌|0|❌|100
C|❌|❌|❌|0|❌|❌
D|❌|0|0|❌|0|❌
E|0|❌|❌|0|❌|100
F|❌|0|❌|❌|0|0

### III

```
Q(C, D) = 0
Q(D, B) = 80
Q(B, F) = 100
```

State / Action|A|B|C|D|E|F
-|-|-|-|-|-|-
A|❌|❌|❌|❌|0|❌
B|❌|❌|❌|0|❌|100
C|❌|❌|❌|0|❌|❌
D|❌|80|0|❌|0|❌
E|0|❌|❌|0|❌|100
F|❌|0|❌|❌|0|0

### IV

```
Q(C, D) = 51.2
Q(D, E) = 80
Q(E, F) = 100
```

State / Action|A|B|C|D|E|F
-|-|-|-|-|-|-
A|❌|❌|❌|❌|0|❌
B|❌|❌|❌|0|❌|100
C|❌|❌|❌|51.2|❌|❌
D|❌|80|0|❌|0|❌
E|0|❌|❌|0|❌|100
F|❌|0|❌|❌|0|0

**b)** `C -> D -> B -> F` (or `C -> D -> E -> F`)

**c)** If the agent was greedy, it could potentially take a suboptimal path when the environment changes, as it is still using the policy for the old environment. If the agent continues to explore the environment, its policy will eventually converge to the optimal policy for the new environment.

**4. a)**



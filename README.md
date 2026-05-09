HTML5

How the physics works, step by step:

Finger flick detection — touchstart records start position/time, touchend records end. The delta gives direction and speed.
Launch velocity — flick speed × scale factor = initial vx/vy. Upward flick = negative vy.
Gravity — each frame: vy += gravity (9.8 scaled). Ball arcs naturally.
Rim collision — two rim endpoints defined. If ball center hits within radius of either rim point, velocity reflects with damping (bounce coefficient ~0.5).
Net detection — if ball passes through the net zone (between rim points, moving downward), it's a score.
Inertia — vx decays slightly each frame via air resistance (vx *= 0.99).

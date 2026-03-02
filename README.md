# CS-230 Portfolio: Draw It or Lose It

## Client + requirements (what they wanted)

The client was The Gaming Room. They had an Android version of Draw It or Lose It and wanted a plan for turning it into a web-based version that can work across platforms. The core requirements I worked around were having games with teams and players, keeping names unique (so people don’t create duplicates), and using unique IDs so everything stays organized when more users are playing.

## What I think I did well

I did best when I stopped rushing into code and actually mapped things out first. Once I had the classes and relationships clear, the patterns made more sense. For example, using a singleton for the service layer helped keep one central place managing the game list and IDs, and using iterator-style searches for name checks matched the “no duplicates” requirement.

## What was helpful about writing the design doc first

The design doc basically saved me time later. When I wrote out the constraints and the domain model, I wasn’t constantly changing my mind while coding. It also forced me to think about stuff that matters in real systems like scaling, storage, and security instead of only focusing on “does it compile.”

## If I could revise one part

If I had to redo one section, I’d improve how I explained the architecture in plain English. I’d add a simple deployment picture (load balancer, app instances, database, image storage/CDN) and I’d be more clear about what data lives where. I’d also tighten the wording in a few places so it’s less “textbook” and more direct.

## How I translated user needs into the design

I kept thinking about what a player would notice first: the game has to feel fast, especially during the image drawing part, and it has to work on different devices without being weird. That’s why I leaned toward a web approach with a clean backend and why I focused on avoiding duplicates and keeping state organized. If you ignore user needs, the system can be technically correct but still annoying to use.

## How I’ll approach design in the future

My process now is: write requirements in plain language, turn them into constraints, sketch the classes and relationships, then pick patterns/tools that fit instead of forcing them in. Next time I’d prototype earlier and test sooner, especially anything involving “many users at once,” because it’s easy to design something that looks fine on paper but doesn’t hold up under load.

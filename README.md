<!-- Zero width character is used to put extra blank lines before and after code -->

<h3>
    
```python
​
from __future__ import annotations

import json
from dataclasses import asdict, dataclass


@dataclass
class Arsenal:
    languages: tuple[str, ...] = ("Python", "JS", "ReactJS", "NestJS")
    databases: tuple[str, ...] = ("SQLite", "MongoDB")
    misc     : tuple[str, ...] = ("Docker", "Webpack")
    ongoing  : tuple[str, ...] = ("React Native", "C++")

    def jsonify(self) -> str:
        return json.dumps(asdict(self), indent=4)


arsenal = Arsenal()
print(arsenal.jsonify())
​
```
</h3>
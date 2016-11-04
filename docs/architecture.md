# Architecture

Some sequence diagram

```sequence
Title: Architecture
A->B: Normal line
B-->C: Dashed line
C->>D: Open arrow
D-->>A: Dashed open arrow
```

![uml](http://www.plantuml.com/plantuml/svg/UDfpLD2rKt2oKl18pSd91m0KGWDz)

Some UML example.

```uml
	Class Stage
	Class Timeout {
			+constructor:function(cfg)
			+timeout:function(ctx)
			+overdue:function(ctx)
			+stage: Stage
	}
	Stage <|-- Timeout
```


``` sequence-hand
Title: Here is a title
A->B: Normal line
B-->C: Dashed line
C->>D: Open arrow
D-->>A: Dashed open arrow
```

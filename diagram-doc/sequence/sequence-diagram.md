[🏠 Back to Home](https://github.com/denitiawan/gropanel-document/blob/main/diagram-doc/README.md)
```
Product Name GroPanel Mobile
```
# Sequence : GroPanel Login

### Diagram
<img src="http://www.plantuml.com/plantuml/svg/ZP5DIiOm443tESLSuBj05zAqXbBiJqdTbv2E4gX9JIRYyIKeIWSHbyE3Do-PEf69b5yEGOuEX1LVCtgB49wWYs4n7WyOmhFpGXXB8KAdvqLEQjZ6kUa79KuJoLbt6a-5jRDMMoFR1pNTSpPA_VZDX60ckDrnGGNg7Mqc_4m0kVIbmhqPGXxo0tW5cyiU5lFt7XREPhZzrgqndS4dXEfBkMPhCIMn8nVpJYQ-FF9_OYPYwF9fDVgzNFy3" width="500">

### Description
### Plan Uml Script
```
@startuml
title Sequence of GroPanel Login

actor GROPANEL_MOBILE
participant GROCORE_BACKEND
participant GROMART_BACKEND

GROPANEL_MOBILE -> GROCORE_BACKEND: Execute Login API
activate GROPANEL_MOBILE
activate GROCORE_BACKEND
GROCORE_BACKEND -> GROMART_BACKEND: Execute Login API
activate GROMART_BACKEND
GROMART_BACKEND --> GROCORE_BACKEND: Response : Login Success
deactivate GROMART_BACKEND
GROCORE_BACKEND --> GROPANEL_MOBILE: Response : Login Success
deactivate GROCORE_BACKEND
deactivate GROPANEL_MOBILE
@enduml
```

# Sequence : GroPanel Activate Account

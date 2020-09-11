# karen-tomayo
# NightClub

Your assignment is to implement a `NightClub` class which admits people into a night club. The NightClub class has a single public method, `AdmitOne`, which simply prints the name of the person admitted into the club based on the requirements described below.

### Requirements:
* Implement the `AdmitOne` method of the `NightClub` interface. `AdmitOne` should print a log message with a timestamp and the name of the person when that person is finally admitted into the nightclub.
* You can only admit one person into the club every 10 seconds. For example, if  `AdmitOne` is called three times (in parallel), it should take ~20 seconds for all three people to be admitted into the club. (person 1 admitted at T-0, person 2 admitted at T-10, and person 3 admitted at T-20)
* Admittance to the club should be first come first serve. In other words, people should be admitted in the same order that `AdmitOne` was called in.

NOTE: You are free to choose any language you are comfortable in.

```golang
type Person struct {
    Name string
}
```

```golang
type NightClub interface {
    // EnterClub blocks until Person p is admitted into the club.
    // Admission to the club should simply print the club-goer's name when
    // the person is admitted into the club.
    EnterClub(p Person)
}
```

### Feature Gates
This page contains an overview of the various feature gates an administrator can specify on different components.

### Overview
Feature gates are a set of key=value pairs that describe features. You can turn these features on or off using the --feature-gates=foo=true,bar=false command line flag on each component.

### Usage
```go
var foo = feature.MustRegister("Foo", false,
	feature.WithFeatureStage(feature.StageAlpha),
	feature.WithFeatureFromVersion("0.0.1"),
	feature.WithFeatureToVersion("1.0.0"),
	feature.WithFeatureDescription("A foo feature"),
)
if foo.Enabled() {
    // TODO Feature
}
```

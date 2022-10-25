# Create a graph of Terraform resources

Terraform has a built-in command to generate a graph of its resources.

```
Usage: terraform [-version] [-help] <command> [args]

Common commands:
graph              Create a visual graph of Terraform resources
```

Invoke the command and convert to a common format as follows.

```
terraform graph | dot -Tsvg > graph.svg
terraform graph | dot -Tpdf > graph.pdf
terraform graph | dot -Tpng > graph.png
```

This is an example graph from the Terraform documentation.

![Sample Graph](https://user-images.githubusercontent.com/773981/197880914-40e1a04e-18a0-4ddd-8887-f66cc014dfce.png)


### Options

```
$ terraform graph --help
Usage: terraform graph [options] [DIR]

  Outputs the visual execution graph of Terraform resources according to
  configuration files in DIR (or the current directory if omitted).

  The graph is outputted in DOT format. The typical program that can
  read this format is GraphViz, but many web services are also available
  to read this format.

  The -type flag can be used to control the type of graph shown. Terraform
  creates different graphs for different operations. See the options below
  for the list of types supported. The default type is "plan" if a
  configuration is given, and "apply" if a plan file is passed as an
  argument.

Options:

  -draw-cycles     Highlight any cycles in the graph with colored edges.
                   This helps when diagnosing cycle errors.

  -module-depth=n  Specifies the depth of modules to show in the output.
                   By default this is -1, which will expand all.

  -type=plan       Type of graph to output. Can be: plan, plan-destroy, apply,
                   validate, input, refresh.
```

## References

1. [Generating Images](https://www.terraform.io/docs/commands/graph.html#generating-images)
1. [Graphviz: How to go from .dot to a graph?](https://stackoverflow.com/a/1494495/6146580)
1. [Graphviz - Graph Visualization Software](https://graphviz.gitlab.io/download/)

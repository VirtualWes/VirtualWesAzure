# Tagging Standards – VirtualWes

## Required Tags (apply to all resources)

| Tag Key       | Example Value     | Purpose                     |
|---------------|-------------------|-----------------------------|
| Environment   | prod / nonprod    | Cost & access control       |
| Owner         | wes               | Accountability              |
| Project       | VirtualWes        | Grouping                    |
| CostCenter    | learning          | Cost allocation             |
| Workload      | shared / web / avd| Logical grouping            |

## Optional but Recommended
- `CreatedBy` = bicep / portal
- `Criticality` = low / medium / high
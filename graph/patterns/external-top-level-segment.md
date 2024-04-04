# `/external` top-level segment

Microsoft Graph API Design Pattern

*The `/external` top-level segment is used to expose data that is provided by third-party services.*


## Problem

Microsoft Graph APIs that build on data or functionality provided by third-parties will want to reference the data from those third-parties.
The third-party data that is exposed on Microsoft Graph should be consistent with the data directly coming from the third-party services, but to be referenced by Graph APIs, CSDL entities need to be created and navigated to.
Doing this allows clients to have their data conveniently in a single API surface, while also maintaining consistency across the Microsoft Graph APIs and the third-party APIs.

## Solution

In addition to the scenario-based APIs, additional APIs should be released under the `/external` top-level segment.
The APIs under `/external` MUST not expose any data that is provided by Microsoft.
Any data that is available under `/external` MUST be data that could be retrieved directly from the third-party service; these APIs are only being added to Graph for convenience and interoperability.

## When to use this pattern

*Describe when and why the solution is applicable and when it might not be.*

## Issues and considerations

Microsoft Graph is not intended to be a single-pane-of-glass for all third-party APIs.
Only APIs that facilitate Graph scenarios should be exposed under `/external`.

## Example

TODO show the EPM APIs that expose external auth system data

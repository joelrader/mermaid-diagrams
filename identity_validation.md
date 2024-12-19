```mermaid
gitGraph

          commit id: "Email Signup" tag: "Start"
          commit id: "Email Reputation Check"
          commit id: "First Factor / Email Verification" tag: "/signup"
          commit id: "Phone Reputation"
          commit id: "Initial Login" tag: "/login"

          branch "Progressive Profiling"
          checkout "Progressive Profiling"
          commit id: "Address Validation"
          commit id: "Identity Documentation Check"
          commit id: "Browser Location Check"
          
          checkout main
          merge "Progressive Profiling" tag: "Mobile App"
          branch "Mobile Device"
          checkout "Mobile Device"
          commit id: "Create Mobile App Session"
          commit id: "Capture ID Documents"
          commit id: "Take Selfie"
          commit id: "Complete Mobile Verification"
          checkout main
          merge "Mobile Device" tag: "/app"
          commit id: "Completed"
```

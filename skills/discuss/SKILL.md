---
name: discuss
description: Conducts in-depth technical interviews about features or tasks using AskUserQuestion, then generates comprehensive specification documents. Use when the user wants to discuss, plan, or spec out a feature/task in detail.
allowed-tools: AskUserQuestion, Write, Read
---

# Feature Discussion & Specification Generator

This skill guides you through conducting comprehensive interviews about features or tasks, then generates detailed specification documents.

## Workflow

### Phase 1: Initial Context Gathering

First, ask the user to describe the task or feature they want to discuss. Use this initial description to understand the domain and scope.

### Phase 2: In-Depth Interview

Use the **AskUserQuestion** tool to conduct a thorough, multi-round interview. Your questions should be:

**Technical Implementation:**
- Architecture and design patterns
- Technology stack choices and justifications
- Data models and schemas
- API design and interfaces
- State management approaches
- Performance considerations
- Scalability requirements
- Integration points with existing systems

**UI & UX (if applicable):**
- User flows and journeys
- Interaction patterns
- Visual design requirements
- Accessibility considerations
- Responsive design needs
- Error states and edge cases
- Loading and feedback mechanisms

**Concerns & Trade-offs:**
- Security implications
- Privacy considerations
- Performance vs. complexity trade-offs
- Maintainability concerns
- Technical debt considerations
- Migration strategies
- Backward compatibility needs

**Non-Obvious Deep Dives:**
- Edge cases and error scenarios
- Failure modes and recovery strategies
- Monitoring and observability
- Testing strategies
- Deployment and rollout plans
- Rollback procedures
- Documentation needs
- Team coordination requirements

**Important Guidelines:**

1. **Avoid obvious questions** - Don't ask generic questions like "What framework do you want to use?" unless truly necessary
2. **Build on previous answers** - Use context from earlier responses to ask increasingly specific questions
3. **Go deep, not wide** - Drill into specific areas rather than surface-level coverage
4. **Continue iteratively** - Keep interviewing until you have comprehensive understanding. Don't rush to completion.
5. **Ask 1-4 questions at a time** - Use the AskUserQuestion tool effectively with focused question sets
6. **Probe assumptions** - Challenge decisions respectfully to ensure they're well-considered

### Phase 3: Completion Signal

Continue the interview until you have exhaustive coverage of:
- All technical requirements and constraints
- Complete user experience vision
- Identified risks and mitigation strategies
- Clear success criteria
- Implementation roadmap

Only proceed to Phase 4 when the user indicates they're satisfied or when you've covered all critical areas comprehensively.

### Phase 4: Specification Generation

Once the interview is complete, generate a comprehensive specification document and write it to a file.

**File Naming:**
- Use a descriptive name based on the feature/task
- Format: `[feature-name]-spec.md`
- Examples: `user-authentication-spec.md`, `payment-integration-spec.md`, `dashboard-redesign-spec.md`

**Specification Structure:**

Use the comprehensive template provided in [spec-template.md](spec-template.md) as your guide. The template includes sections for:
- Overview and goals
- User stories and use cases
- Technical requirements (architecture, tech stack, data model, API design, state management)
- UI/UX requirements (flows, design, accessibility)
- Non-functional requirements (performance, security, scalability, reliability)
- Edge cases and error handling
- Testing strategy
- Deployment plan
- Risks and mitigation
- Implementation phases
- Success criteria
- References

**Important:** Adjust the structure based on what was discussed. Remove sections that aren't relevant, add sections for unique aspects of the feature.

## Example Interaction Flow

```
User: /discuss
You: Let me help you develop a comprehensive specification. Please describe the task or feature you'd like to discuss in detail.

User: [Describes feature]

You: [Uses AskUserQuestion with 2-3 deep technical questions]

User: [Answers]

You: [Uses AskUserQuestion with follow-up questions based on answers]

... [Multiple rounds of deep questioning] ...

You: [Once complete, generates and writes spec file]
I've created a comprehensive specification document at: [filename].md
```

## Notes

- Prioritize depth over breadth
- Challenge assumptions constructively
- Ensure all trade-offs are explicitly discussed
- The specification should be detailed enough that another developer could implement it
- If the user seems uncertain, ask more questions rather than making assumptions

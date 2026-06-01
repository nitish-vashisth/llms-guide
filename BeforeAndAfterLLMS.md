# Software Engineering Before LLMs vs After LLMs: What Actually Changed?

A common narrative suggests that AI has fundamentally changed software engineering because it can write code.

That is true, but it is also an oversimplification.

The more important change is not that AI can generate code. The more important change is that AI can now participate in almost every phase of the Software Development Lifecycle (SDLC).

It can help research requirements.

It can generate design documents.

It can propose architectures.

It can create implementation plans.

It can write code.

It can generate unit tests.

It can review pull requests.

It can suggest optimizations.

It can even explain production incidents.

For the first time, engineers have access to a system that can contribute across the entire development lifecycle rather than just one activity.

And that changes the nature of software engineering itself.

## Software Engineering Before LLMs

Before LLMs became mainstream, software development was a relatively linear process.

Requirements were gathered through conversations with stakeholders.

Engineers spent time understanding business problems and translating them into technical requirements.

Design discussions happened through architecture reviews, whiteboard sessions, and design documents.

Implementation was largely manual.

Developers wrote code line by line.

Documentation was often created after implementation.

Code reviews focused on logic, correctness, maintainability, and adherence to architectural standards.

Testing required deliberate effort.

Every piece of code represented human thought and human labor.

The process was slower, but something important happened during that slowness.

Validation was naturally embedded into development.

As developers wrote code, they continuously evaluated it.

They thought about edge cases.

They reconsidered assumptions.

They mentally simulated execution paths.

They refactored when something felt wrong.

They gradually built a mental model of both the problem domain and the codebase.

By the time code reached a pull request, the engineer had often interacted with that code dozens of times.

They had already reviewed it while writing it.

They had already tested it while building it.

They had already challenged many of their own assumptions.

The act of writing code was itself a validation mechanism.

This wasn't perfect. Bugs still existed. Poor designs still happened.

But the process naturally forced engineers to stay deeply engaged with the system they were building.

## Software Engineering After LLMs

Today the workflow looks very different.

An engineer can describe a feature and receive hundreds or thousands of lines of code within seconds.

The same system can generate design options, architecture diagrams, migration plans, test cases, and documentation.

The speed is remarkable.

Tasks that previously required hours can often be completed in minutes.

But speed changes behavior.

When code becomes cheap to generate, the bottleneck shifts elsewhere.

The bottleneck is no longer code creation.

The bottleneck becomes understanding and verification.

Consider a modern workflow.

An engineer asks an AI assistant to:

* Analyze requirements
* Generate a technical design
* Propose multiple implementation approaches
* Write the code
* Generate tests
* Review the implementation

The engineer may receive a complete solution before fully developing their own mental model of the problem.

This is where things become interesting.

Historically, understanding happened before implementation.

Now implementation can happen before understanding is complete.

That inversion creates entirely new risks.

## The Hidden Value of Manual Development

Many engineers underestimate what they gained from manually building software.

The value was not merely typing code.

The value was developing context.

When developers spent days implementing a feature, they naturally learned:

* Why the feature existed
* How it interacted with adjacent systems
* What assumptions were being made
* Where edge cases existed
* Which architectural constraints mattered

This understanding accumulated gradually.

Modern AI tools can compress implementation time dramatically.

What they cannot automatically compress is understanding.

The risk is that engineers begin shipping code faster than they are building understanding.

And when understanding grows slower than implementation, problems start to appear.

## Why Traditional Validation Is No Longer Enough

Many teams respond by saying:

"We already have static analysis."

"We already have code reviews."

"We already have CI/CD."

"We already have testing."

Those tools remain valuable.

But most of those systems were designed for a world where humans produced code at human speed.

They were never designed to evaluate thousands of lines of AI-generated code produced in minutes.

Consider code review.

Historically, a reviewer examined code written by another engineer who understood every line they submitted.

Today, reviewers are often examining code generated by a system that neither the author nor the reviewer fully understands.

The scale changes.

The dynamics change.

The risks change.

Traditional quality gates still matter.

But they are no longer sufficient on their own.

The challenge is no longer detecting syntax errors.

The challenge is detecting incorrect assumptions, architectural inconsistencies, hidden complexity, and subtle design flaws that accumulate over time.

## Why AI Sometimes Produces Bad Software

Many discussions stop at a simple explanation:

"LLMs hallucinate."

While technically true, that explanation is incomplete.

The deeper issue lies in how these systems work.

An LLM does not understand software architecture in the way experienced engineers do.

It does not possess a mental model of your business.

It does not understand organizational priorities.

It does not reason from first principles.

It predicts the next most probable token based on patterns observed during training and the context provided in the prompt.

This approach is incredibly powerful.

It is also fundamentally probabilistic.

When given good context, good requirements, and strong constraints, the output can be excellent.

When given incomplete, ambiguous, outdated, or incorrect information, the model will often confidently continue in the wrong direction.

The model cannot reliably distinguish between:

* Missing information
* Incorrect information
* Contradictory information

It simply attempts to generate the most statistically plausible continuation.

This explains why AI-generated code can appear highly professional while being fundamentally incorrect.

The code looks convincing because the model is exceptionally good at reproducing patterns associated with convincing code.

Correctness, however, is a separate problem.

## The Architecture Problem

The greatest risk is rarely individual bugs.

Most bugs can be fixed.

The larger danger is architectural degradation.

AI is often excellent at producing locally correct solutions.

A method works.

A class compiles.

A test passes.

A feature ships.

The problem emerges when hundreds of these local optimizations accumulate over months.

One feature introduces a new abstraction.

Another bypasses an existing pattern.

A third duplicates functionality that already exists elsewhere.

Each change appears reasonable in isolation.

Collectively, they slowly erode architectural consistency.

Over time teams experience:

* Duplicate abstractions
* Inconsistent patterns
* Boundary violations
* Cross-layer dependencies
* Increasing coupling
* Growing complexity

No single pull request causes the problem.

The architecture slowly drifts away from its original intent.

This phenomenon is becoming one of the defining risks of AI-assisted development.

Not because AI is uniquely flawed.

But because AI naturally optimizes for local success while architecture requires global consistency.

## The New Engineering Challenge

The challenge facing modern engineering teams is not how to generate more code.

AI has largely solved that problem.

The challenge is ensuring that rapidly generated software remains understandable, maintainable, consistent, and aligned with long-term architectural goals.

In many ways, software engineering is returning to its original purpose.

The profession was never fundamentally about typing code.

It was about making good decisions under uncertainty.

AI changes how software is produced.

It does not eliminate the need for judgment.

In fact, it may increase it.

And that leads to the next question:

If AI can generate code, tests, designs, and documentation faster than humans ever could, what new failure modes emerge when humans begin trusting those outputs too quickly?

That is where we encounter verification blindness, architectural drift, context collapse, unsafe tooling, and the other challenges defining the next generation of software engineering.

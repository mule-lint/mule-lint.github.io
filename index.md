---
layout: page
---

<div class="full-width top-bottom-pad">
  <div class="container main-content">
    <div class="row">
      <div class="col-md-12">
        <h1>Mule Lint</h1>

        <p>The mule-lint application is an open source project to provide basic
        static analysis checking of certain elements of a Mule Integration
        Application. This is a growing concern and a project has been spun up
        to help fill this gap. This open source project was started by Chad
        Gorshing, an Independent MuleSoft Certified Consultant (not an employee
        of MuleSoft, but has partnered on multiple occasions), and features are
        still being developed.</p>

        <p>Rules are intended to be re-usable across many teams, where as the options could be team specific (files to ignore, dictionary)</p>

        <p>There are "rules" that need to be checked that have specific use
        cases and a predefined rules can not be already created. So as a guide,
        here are a few things to keep in mind on what could fit for your
        business use cases.</p>

        <p>Many "rules" are still subjective and we continually are learning
        what rules can easily work and be a good foundation for others to
        follow.</p>
      </div>
    </div>
  </div>
</div>

<div class="full-width top-bottom-pad alternating-row">
  <div class="container main-content">
    <div class="row">
      <div class="col-md-12">
        <h1 class="section-heading">Workflow</h1>
      </div>
    </div>

    <div class="row">
      <div class="col-md-3">
      </div>

      <div class="col-md-9">
        <h3>Running as part of your build</h3>

        <p>Currently this project will not cause a build failure, but only
        provide information for others to act upon. Teams will need to decide
        for themselves what constitutes a failure for their cases.  Just
        because a rule is "broken" once does not necessarily warrant a build or
        deployment failure.  We feel that this is up the team to decide what
        level is good for them to proceed (if any at all).</p>

        <p>We would love to hear what features you would like next by opening an
        issue on <a href="https://github.com/nuisto/mule-lint/issues">Github</a>.
        </p>
      </div>
    </div>
  </div>
</div>

<div class="full-width top-bottom-pad">
  <div class="container main-content">
    <div class="row">
      <div class="col-md-12">
        <h1 class="section-heading">Complexity</h1>
      </div>
    </div>

    <div class="row">
      <div class="col-md-9">
        <h3>Cyclomatic Complexity</h3>

        <p>If you have been a part of a Mule project for a length of time, then I'm sure you have ran into flows that were just too big and needed to be broken down. This makes things easier for testing, understanding by others and your future self, follow single responsibility and so on.</p>

        <p>How can we bring some of these well known metrics into the Mule world, after all <a href="https://confluex.com/blog/integration-software-is-software/">Integration Software is Software</a>. Mule poses an interesting spin on this topic with
        different message processors; filters, flow-refs, DataWeave,
        components (Java classes).
        </p>
      </div>

      <div class="col-md-3">
      </div>
    </div>

    <div class="row">

      <div class="col-md-3">
      </div>
      <div class="col-md-9">
        <h3>We Aren't There Yet</h3>

        <p>We don't have a solution for this, but is something we are discussing with various developers and consultants we have wide experience we can learn from. We are very interested in getting feedback from the community as well. As things progress we will be creating technical documentation and linking to it on this site.</p>

      </div>

    </div>

  </div>
</div>

<!--
See git history on other ways to align the text and use col-md-8 to tighten up the paragraphs
Possible other ideas
Getting started
Next Steps or Advanced Guide
Main concepts
Contributing
FAQ

-->

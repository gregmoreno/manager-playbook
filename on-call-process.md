# On-Call Process

## Objective

Handle exceptional situations. Exceptional situations are outages, and anything that, if left unattended, would lead to an outage.

## Operating Principles

- At any given time at least 1 engineer is responsible for attending exceptional issues.
- The engineer should remain contactable for the duration of the oncall shift.
- The on-call engineer should mitigate the impact of the issue whatever means necessary including shortcut solutions that will not solve the problem in the long term.
- If the on-call engineer cannot resolve the issue or does not acknowledge the alert, there is an escalation system whereby other engineers become involved.
- The on-call engineer is responsible for all communication and coordination regardless if the issue was escalated to other engineers.
- After the issue is managed, follow-up work should be done during normal business hours - root cause analysis, postmortems, and working on long-term solutions.

## OnCall Calendar

- An engineer is oncall for one week at a time.
- Each engineer should have at least 2 weeks between oncall shifts to work on projects on normal hours.

## OnCall Readiness

The oncall engineer should check the following during normal business hours:

- Check access to resources - e.g. logins, VPNs
- Check laptop/charger, phone are ready (especially if remote)
- Check access to playbooks.

## Being OnCall

- Once alerted, acknowledge the alert so it will not escalate.
- Triage → Coordinate → Mitigate → Resolve → Followup
- **Triage**
    - As quickly as possible, figure out what the problem might be, what is the impact, how severe the incident is, who can fix the problem.
- **Coordinate**
    - If the on-call engineer cannot mitigate the issue, escalate the issue to other engineers who can.
    - Coordinate and communicate in a designated chat channel.
    - Start extensive documentation and tracking of the details of mitigation.
    - Tip: Post in the channel what you are working on, new problems that came-up, actions you have taken, blockers. This will be useful in creating the incident report later.
- **Mitigate**
    - Work to mitigate the impact of the incident without root-causing, and importantly, not to fix the problem at all.
    - Reduce the impact and make sure customers are no longer affected.
- **Resolve**
    - Work to resolve the incident after it has been mitigated.
    - Identify root cause and work on fix. This might take a while and can be done on normal business hours.
    - Resolution should be treated with the same caution as feature deployments, i.e. do not introduce a new problems, avoid hotfixes as much as possible.
- **Follow-Up**
    - Incident is examined, discussed, and learned from.
    - Document in a post-mortem document or incident report
    - Track indicators:
        - technical cause: lack of testing, untested failure, deployment failure
        - component where the incident started
        - re-occurrence or not
    - The oncall engineer takes the lead, organizing and running postmortem reviews.
    - Update the playbook if necessary (e.g. use of better tools)

## Postmortems

- Written by the on-call engineers with input from other engineers if issue was escalated.
- Good postmortems are blameless.
- Include the following:
    - Short description of the incident
    - Evaluation of the severity and impact
    - Root cause
    - Timeline of the incident and account how it was triaged, mitigated, and resolved.
    - List of things that went well and didn't go well.
    - List of follow-up tasks and possible long-term solutions

## End of Shift

- Send a report that includes any notable events the next engineer needs to know, manual monitoring that needs to be done, updates to the playbook.

## Playbook

- A list of procedures and things to check or do for any given alert.
- The playbook should be updated when new issues are encountered.
- Details can vary depending on your team's experience.

## Long-Term Improvements

- Training plan as part of onboarding process. New engineers should be able to take oncall shifts on Month 4.
- “Game Day” exercises.
- Regular stress testing and failover testing.
- Monitoring for “sick” systems rather than “down” systems.
- Active monitoring of website resources (e.g. alert is triggered when website is not accessible)
- Implement SLAs and track violations.

## Assessment Questions:

- How are outages detected? (automatic monitoring? customer complaints?)
- Is there a playbook for common failover scenarios and outage-related duties?
- Is there an oncall calendar?
- How is the oncall calendar created?
- Can other regions cover for each other other for extended periods of time?
- Do you write postmortems or incident reports? Is there a deadline for when a postmortem must be completed?
- Is there a standard template for postmortems?
- Are postmortems reviewed to assure actions are completed?
- Is there a process to triage recommendations in postmortems?
- Do you frequently do stress testing and failover testing? (quarterly or monthly?)
- Do you do "game day" exercises?
- Is there a monitoring before outages occur, i.e. indications of "sick" systems rather than done "down" systems.
- Is the SLA actively defined and measured? e.g. initial, hands-on-keyboard, issue resolved, postmortem complete.

### References

- [Increment On-Call](https://increment.com/on-call/)
- [The Practice of Cloud System Administration](https://www.amazon.ca/Practice-Cloud-System-Administration-Practices/dp/032194318X/ref=tmm_pap_swatch_0?_encoding=UTF8&qid=1585113269&sr=8-1)
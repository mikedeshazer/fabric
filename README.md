The original docs for this was a bit tacky. Consensus in  a blockchain is important, and the Fabric devs didn't really do into details about this fact in the original Fabric Readme... To be clear, that readme is below, and says look elsewhere. Those docs aren't so clear either. It's a new project. We're trying to help. 'Cuase this could be grat. (This README will be made much more professionally once this repo solves some problems :)) This project is to fix  Hyperledgers fabric glaring consensus problems. And also... you shouldn't be able to turn off a blockchain when it's distributed. Gonna work on that one, too.
Note: Hyper dev mode. Maybe that's what Hyperledger in general should be called right now. There is still hope. Okay...
If this code doesn't work correctly, as is, then here is something you should know. Try that, then check out the rest of the docs below. Message me as mike@thinkathon.io if you have issues. I get back pretty quickly.

Using a Consensus Plugin

A consensus plugin might require some specific configuration that you need to set up. For example, to use the Practical Byzantine Fault Tolerant (PBFT) consensus plugin provided as part of the fabric, perform the following configuration:

In core.yaml, set the peer.validator.consensus value to pbft
In core.yaml, make sure the peer.id is set sequentially as vpN where N is an integer that starts from 0 and goes to N-1. For example, with 4 validating peers, set the peer.id tovp0, vp1, vp2, vp3.
In consensus/pbft/config.yaml, set the general.mode value to batch and the general.N value to the number of validating peers on the network, also set general.batchsize to the number of transactions per batch.
In consensus/pbft/config.yaml, optionally set timer values for the batch period (general.timeout.batch), the acceptable delay between request and execution (general.timeout.request), and for view-change (general.timeout.viewchange)
**Note:** This is a **read-only mirror** of the formal [Gerrit](https://gerrit.hyperledger.org/r/#/admin/projects/fabric) repository,
where active development is ongoing. Issue tracking is handled in [Jira](https://jira.hyperledger.org/secure/RapidBoard.jspa?projectKey=FAB&rapidView=5&view=planning)


## Incubation Notice

This project is a Hyperledger project in _Incubation_. It was proposed to the
community and documented [here](https://goo.gl/RYQZ5N). Information on what
_Incubation_ entails can be found in the [Hyperledger Project Lifecycle
document](https://goo.gl/4edNRc).

[![Build Status](https://jenkins.hyperledger.org/buildStatus/icon?job=fabric-merge-x86_64)](https://jenkins.hyperledger.org/view/fabric/job/fabric-merge-x86_64/)
[![Go Report Card](https://goreportcard.com/badge/github.com/hyperledger/fabric)](https://goreportcard.com/report/github.com/hyperledger/fabric)
[![GoDoc](https://godoc.org/github.com/hyperledger/fabric?status.svg)](https://godoc.org/github.com/hyperledger/fabric)
[![Documentation Status](https://readthedocs.org/projects/hyperledger-fabric/badge/?version=latest)](http://hyperledger-fabric.readthedocs.io/en/latest/?badge=latest)

## Hyperledger fabric

The fabric is an implementation of blockchain technology, leveraging familiar
and proven technologies. It is a modular architecture allowing pluggable
implementations of various function. It features powerful container technology
to host any mainstream language for smart contracts development.

## Documentation, Getting Started and Developer Guides

This is a **read-only mirror** of the formal Gerrit repository, please visit our
[online documentation](http://hyperledger-fabric.readthedocs.io/en/latest/) for
information on getting started using and developing with the fabric, SDK and chaincode.

## Contributing

We welcome contributions to the Hyperledger Project in many forms. There’s always plenty to do!
Full details of how to contribute to this project are documented [here](http://hyperledger-fabric.readthedocs.io/en/latest/CONTRIBUTING/).

## Community

[Hyperledger Community](https://www.hyperledger.org/community)

[Hyperledger mailing lists and archives](http://lists.hyperledger.org/)

[Hyperledger Slack](http://hyperledgerproject.slack.com) - if you need an invitation, try our [Slack inviter](https://slack.hyperledger.org)

[Hyperledger Wiki](https://github.com/hyperledger/hyperledger/wiki)

[Hyperledger Code of Conduct](https://github.com/hyperledger/hyperledger/wiki/Hyperledger-Project-Code-of-Conduct)

[Community Calendar](https://github.com/hyperledger/hyperledger/wiki/PublicMeetingCalendar)

## License <a name="license"></a>
The Hyperledger Project uses the [Apache License Version 2.0](LICENSE) software
license.

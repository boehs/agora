# Welcome to the Agora!
This is an [Agora](https://flancia.org/agora). You can find a reference implementation live at <https://anagora.org/>.
This Agora's architecture has several components distributed over three git repositories:

- The Agora *root repository*, which you are browsing: <https://github.com/flancian/agora>. 
  - This root repository contains a high level definition of the Agora as expressed by the list of digital gardens integrated into it (`gardens.yaml`) and the contract agreed upon by the community (`CONTRACT.md`).
- The *Agora Server*, <https://github.com/flancian/agora-server>.
  - Which contains a reference Python / Flask web app that integrates and serves content. It is live at <https://anagora.org>.
- The *Agora Bridge*, <https://github.com/flancian/agora-bridge>.
  - Which contains a set of processes to retrieve Agora content.

# To join

If you would like to join the reference Agora described in this particular repository, please send a PR adding your garden to `gardens.yaml` or reach out to [flancian](https://anagora.org/flancian) or a member of the [fedstoa](https://anagora.org/fedstoa) with a pointer to your content and a choice of username. 

After being integrated, your garden will appear live at <https://anagora.org/@username> and your notes will be integrated into the Agora; this means that if you volunteer a note named ```foo.md```, it will show up in node <https://anagora.org/foo> together with all similar notes by other Agora users.

# To run

To run the reference Agora: 

- Clone all three repositories described above (ideally under a dedicated user) in some user's $HOME directory (not strictly needed, but scripts are tested in a setup like this).
- Install Python requirements in each of `agora-server` and `agora-bridge`, ideally in a virtual environment: `python3 -m venv; . venv/bin/activate; pip3 install -r requirements.txt`.
- In `agora`: run `bin/pull` in agora to start periodically retrieving the digital gardens defined in `gardens.yaml`.
- Run `./run-dev.sh` or `./run-prod.sh` (requires further web server configuration) in `agora-server` to start the web interface.

Of course you are also free to run your own Agora! To do this, just run the bridge against a local `gardens.yaml` file -- or fork the root repository and adjust as wished. As usual please reach out if you need a hand with anything :)

# Wait, what's an Agora again?

An [Agora](https://anagora.org/wiki/Agora) is a distributed, goal-oriented social network operating on a cooperatively built and maintained knowledge graph. The implementation you are currently looking at tries to assemble such a graph out of a collection of [digital gardens](flancia.org/go/garden), but other data sources are coming.

You can view the Agora at <https://anagora.org>. For how to write to it: if you take personal digital notes with some system such as [foam](https://anagora.org/foam) or [obsidian](https://anagora.org/obsidian), you are most of the way there; all you need to do is share them with the Agora (see "join" above). If you don't, but you would like to, please refer to [agora client](https://anagora.org/agora-join) or reach out!

# Contract
***If you contribute directly to an Agora you are assumed to be in agreement with its then current contract.*** 

Please refer to the Agora's [contract](https://anagora.org/contract), in particular as posted by the system account @agora (which is binding for all users).

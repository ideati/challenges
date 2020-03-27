# Rouge
This challenge is not a contest, is a call to arms.

## Context
Wordpress runs a big portion of the world web pages. For this, there are many rogue actors trying to exploit vulnerabilities. Each intent to access to a WordPress related link could be considered as a rogue agent and the ip address should be reported and banned.
But this is such a mild answer to a thief. What happens if we send a response to a `GET /wp-login.php` with a careful crafted routine that would pass for a succesful attack but in reality it start consuming the attacker resources. One lonely site may not do a lot of damage, but if more sites unites to the cause, the balance of power will change for attackers.

## Objective
Create a Pandora's box to give to an attacker in order to feign a succesful attack to WordPress but instead, consume resources on the attacker machine.

## License
Each author retains the rights to his/her code, but each entry shall have a OSI approved license in order to be considered for participation.

## Restrictions
- Use any programming language, library or tool.
- Nothing else. Everything goes. The most time our code runs on attacker's machine the better. Try to allocate memory, spawn processes, run long loops while avoiding detection. It is better to avoid causing spikes in consumption that could be easily detected. Instead, a long running routine who causes a constant consumption may be a better choice.
- Let's give them a taste of their own medicine.

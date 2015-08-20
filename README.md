# api_wordlist
A wordlist of API names used for fuzzing web application APIs.

## Contents
* api_seen_in_wild.txt - This contains API function names I've seen in the wild.
* actions.txt - API function name verbs
* objects.txt - API function name nouns
* preambles.txt - Common API function name preambles that may occur prior to verbs or nouns

## Usage
 1. In burpsuite, send an API request you want to fuzz to Intruder. 
 2. Remove the existing API function call, and replace it with two § characters for each text file you want to use for fuzzing.
 3. On the "Positions" tab, set Attack type to "Cluster Bomb" 
 4. On the "Payloads" tab, select 1 for the fist Payload set drop-down, then select a Payload type of "Runtime file" and navigate to the directory you downloaded these text files to. Select "preambles.txt".
 5. Repeat step 4 by setting Payload set 2 to "actions.txt" and Payload set 3 to "objects.txt"
 6. Start attack

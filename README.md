# FasterCrypt_docs
# FasterCrypt
FasterCrypt is a competition to optimize 3 encryption algorithms which are used in the PacketCrypt bandwidth hard proof of work. These encryption algorithms are also used in many other software programs so the results of this competition will benefit the entire internet ecosystem.

## Algorithms
The FasterCrypt competition will focus on optimization of three key encryption algorithms used in the popular libsodium encryption library.

- ChaCha20 stream cipher
	- crypto_stream_chacha20_ietf
	- crypto_stream_chacha20_ietf_xor_ic
- Poly1305 authenticator
	- crypto_onetimeauth_poly1305_init
	- crypto_onetimeauth_poly1305_update
	- crypto_onetimeauth_poly1305_final
- Blake2b hashing algorithm
	- crypto_generichash_blake2b

## Process
1. Judges will test the unmodified algorithms on the target hardware and publish the resulting performance, this will become the mark to beat.
2. Applicants submit their improved algorithms to the competition judges by the deadline (TODO).
	- Proposals will remain under embargo until the applicant has won, or is eliminated from the competition
	- Applicants MAY submit before the deadline for validation from the judges of the correctness of their application.
3. After the deadline, judges will test the applications on the target hardware (TODO) and publish the results of testing
	- All submissions which:
		1. Are in violation with the rules of the competition, or
		2. Do not test better than the mark to beat

	- will be eliminated from the competition and the embargo on release of their code will end.
	- If a submission is deemed to be slightly outside of the rules, for example a deficiency of code style, the judges may at their sole descretion tenatively accept the submission, allowing the contestant to cure deficiencies in the following round.
4. After results have been published, the fastest proposed implementation will now become the mark to beat and applicants will have Five (5) days to re-submit.
	- Re-submission will return the process to step 2.
5. When there is only 1 candidate remaining, they will be declared the winner and the embargo on their submission will end.
	
## Possibility for further rounds
If it is agreed between the winning candidate and the competition administrators, another round may be added:

- The process will return to step 2, but with anyone from the public able to enter
- The bounty for final win will be raised
- The current winning candidate's submission will remain under embargo

## Submission Rules
1. Submissions must consist only of modifications to existing software:
	- packetcrypt_rs
	- libsodium
	- sodiumoxide
2. All modifications of software shall bear the same open source license as the software that is being modified.
3. No judge shall disclose any information regarding the code or techniques used in any of the submissions under embargo to any other person who is not a judge, including to administrators of the competition.
4. When embargo is lifted on a submission, the submission shall be published by the judge to a public git repository.
5. All modifications of software must adhere to the coding convensions of the software which they modify, this is subjective and will be decided by the judges but the following are some guidelines to inform the definition of compliance:
	- They must compile using the same compilation process as the original software
	- No tests should fail which previously were passing and no tests should be removed
	- The software should work on the same operating systems and processor architectures that it worked on before, any use of assembly instructions which are not available on all processors should use runtime checks to enable itself where available
	- Code style convensions should be adhered to



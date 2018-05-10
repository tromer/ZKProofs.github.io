## What is a zero-knowledge proof?

- [Zero Knowledge Proofs: An illustrated primer](https://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/)
- [What are zk-SNARKs?](https://z.cash/technology/zksnarks.html)
- ["The Functionality of zk-SNARK"](http://qed-it.com/2017/07/challenge-one-the-functionality-of-zk-snark/) challenge set in ["The Hunting of the SNARK"](http://qed-it.com/2017/07/the-hunting-of-the-snark/).
- ["Probabilistic Proof Systems"](http://people.cs.georgetown.edu/jthaler/COSC544.html) course notes

## Zero-knowledge proving systems

- [[GGPR13]](https://eprint.iacr.org/2012/215)
  - [Pinocchio [PGHR13]](https://eprint.iacr.org/2013/279.pdf)
  - [[BCGTV13]](https://eprint.iacr.org/2013/507)
  - [Geppetto [CFHKKNPZ14]](https://eprint.iacr.org/2014/976)
  - [[BCTV14a]](http://eprint.iacr.org/2013/879)
- [[BCTV14b]](https://eprint.iacr.org/2014/595)
- [[CTV15]](https://eprint.iacr.org/2015/377)
- [ZKBoo [GMO16]](https://eprint.iacr.org/2016/163.pdf)
- [[Groth16]](https://eprint.iacr.org/2016/260.pdf)
- [[BCC+16]](https://eprint.iacr.org/2016/263.pdf)
  - [Bulletproofs [BBBPWM17]](https://web.stanford.edu/~buenz/pubs/bulletproofs.pdf)
- [ZKB++ / Picnic [CDGORRSZ17]](https://eprint.iacr.org/2017/279.pdf)
- [Ligero [AHIV17]](https://acmccs.github.io/papers/p2087-amesA.pdf)
- [Hyrax [WTSTW17]](https://eprint.iacr.org/2017/1132.pdf)
- [zk-STARKs [BBHR18]](https://eprint.iacr.org/2018/046)
- [Updatable Universal CRSs [GKMMM18]](https://eprint.iacr.org/2018/280)

## Implementations of proving systems

- [libsnark](https://github.com/scipr-lab/libsnark) - C++ library for zk-SNARK proofs
  - [[GGPR13]](https://eprint.iacr.org/2013/279.pdf) (implements [[BCTV14a]](http://eprint.iacr.org/2013/879) approach)
  - [[BCTV14b]](https://eprint.iacr.org/2014/595)
  - [[CTV15]](https://eprint.iacr.org/2015/377)
- [bellman](https://github.com/ebfull/bellman/) - Rust library for zk-SNARK proofs
  - [[Groth16]](https://eprint.iacr.org/2016/260.pdf)
- [ZKBoo](https://github.com/Sobuno/ZKBoo)
- [[BCC+16]](https://eprint.iacr.org/2016/263.pdf)
  - [BulletProofLib](https://github.com/bbuenz/BulletProofLib) (implements [Bulletproofs [BBBPWM17]](https://web.stanford.edu/~buenz/pubs/bulletproofs.pdf) approach)
  - [secp256k1-zkp (experimental)](https://github.com/ElementsProject/secp256k1-zkp/pull/16) (implements [Bulletproofs [BBBPWM17]](https://web.stanford.edu/~buenz/pubs/bulletproofs.pdf) approach)
  - [ristretto-bulletproofs](https://github.com/chain/ristretto-bulletproofs/) (implements [Bulletproofs [BBBPWM17]](https://web.stanford.edu/~buenz/pubs/bulletproofs.pdf) approach using Ristretto on Curve25519) ([notes](https://doc-internal.dalek.rs/ristretto_bulletproofs/notes/index.html))
- Picnic
  - [Reference implementation](https://github.com/Microsoft/Picnic)
  - [Optimized implementation](https://github.com/IAIK/Picnic)
- [libSTARK](https://github.com/elibensasson/libSTARK)
  - [zk-STARKs [BBHR18]](https://eprint.iacr.org/2018/046)
- [emmy](https://github.com/xlab-si/emmy)
  - ZKP primitives for [Camenisch-Lysyanskaya anonymous credentials](https://eprint.iacr.org/2001/019.pdf)
  - Camenisch-Lysyanskaya anonymous credentials (work in progress)
  - client-server (prover-verifier) communication based on Protobuffers and gRPC
- [VC](https://archive.codeplex.com/?p=vc) implementation accompanying the [Pinocchio [PGHR13]](https://eprint.iacr.org/2013/279.pdf) and [Geppetto [CFHKKNPZ14]](https://eprint.iacr.org/2014/976) papers

## Low-level libraries/languages for writing circuits

- [libsnark](https://github.com/scipr-lab/libsnark)'s gadgetlib1 and gadgetlib2 - C++ libraries for for building circuits for preprocessing zk-SNARKs
- [jsnark](https://github.com/akosba/jsnark) - Java library for building circuits for preprocessing zk-SNARKs, backed by libsnark
- [ZoKrates](https://github.com/JacobEberhardt/ZoKrates) - Toolbox for zk-SNARKs on Ethereum, backed by libsnark
- [Snarky](https://github.com/o1-labs/snarky) - OCaml front-end for writing R1CS SNARKs, currently backed by libsnark

## General-purpose compilers from high-level languages
- [ZKPDL [MEKHL10]](https://www.usenix.org/legacy/event/sec10/tech/full_papers/Meiklejohn.pdf)
  - [Cashlib](https://github.com/brownie/cashlib) - C++ implementation
- [Pinocchio [PGHR13]](https://eprint.iacr.org/2013/279.pdf)
- [Pantry [BFRSBW13]](https://arifeldman.com/pub/pantry-sosp13.pdf)
- [Geppetto [CFHKKNPZ14]](https://eprint.iacr.org/2014/976)
- [TinyRAM [BCGTV13]](https://eprint.iacr.org/2013/507), [vnTinyRAM [BCTV14a]](http://eprint.iacr.org/2013/879) and [scalable TinyRAM [BCTV14b]](https://eprint.iacr.org/2014/595)
- [Buffet [WSRBW15]](https://cs.nyu.edu/~mwalfish/papers/buffet-ndss15.pdf)
- [C0C0 [KZMQCPPSS15]](https://eprint.iacr.org/2015/1093)
- [Pequin](https://github.com/pepper-project/pequin) - Toolchain to verifiably execute programs expressed in (a large subset of) C,  backed by libsnark.
  - [Relevant publications](https://www.pepper-project.org/#publications) 
- [Snårkl [SML17]](https://link.springer.com/chapter/10.1007%2F978-3-319-73305-0_3) - Haskell embedded DSL for verifiable computing
  - [Implementation backed by libsnark](https://github.com/gstew5/snarkl)
- [xJsnark [KPS18]](https://csdl.computer.org/csdl/proceedings/sp/2018/4353/00/435301a543.pdf)


## Example circuits

- [Zcash Sprout](https://github.com/zcash/zips/blob/master/protocol/protocol.pdf)
  - Based on [Zerocash [BCGGMTV14]](https://www.ieee-security.org/TC/SP2014/papers/Zerocash_c_DecentralizedAnonymousPaymentsfromBitcoin.pdf)
  - [C++ implementation over BN128 using libsnark](https://github.com/zcash/zcash/tree/master/src/zcash/circuit)
  - [Rust implementation over BLS12-381 using bellman](https://github.com/zcash-hackworks/sapling-crypto/tree/master/src/circuit/sprout)
- [ANONIZE [HMP15]](https://eprint.iacr.org/2015/681.pdf)
  - [Mobile applications (closed-source)](https://anonize.org/)
- [Zcash Sapling](https://github.com/zcash/zips/blob/master/protocol/sapling.pdf)
  - [Rust implementation over BLS12-381 using bellman](https://github.com/zcash-hackworks/sapling-crypto)

## Standardization efforts

- [Zero Knowledge Proof Standardization](https://zkproof.org/) and [1st Workshop](https://zkproof.org/standards_meetings.html)
- [Letter to NIST](docs/Letter-to-NIST-20160613-Advanced-Crypto.pdf) on standardizing new cryptographic standards


## So are they fast yet?

Stay tuned! 😁

## Improve this page

Additions, corrections and other suggestions are welcome! You can propose an edit to this page [here](https://github.com/ZKProofs/ZKProofs.github.io/edit/master/index.md). (Note that after making your edits, there are several confirmations to click through in order to create the "pull request" in the Git repository underlying this page.)

For more broad changes, you can make a pull request [here](https://github.com/ZKProofs/ZKProofs.github.io)!

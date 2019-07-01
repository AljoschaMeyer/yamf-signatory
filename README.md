# YAMF-Signatory

> Yet-Another-Multi-Format - Signatory

Self-describing public keys for asymmetric digital signatures.

A yamf-signatory is a pair of a numeric identifier for a signature scheme, and a public key. The currently supported schemes:

| Signature Scheme                     | Numeric Id | Public Key Length (Bytes) |
|--------------------------------------|------------|---------------------------|
| [Ed25519](https://ed25519.cr.yp.to/) | 0          | 32                        |

## Binary Encoding

The binary encoding of a yamf-signatory is the binary [stlv](https://github.com/AljoschaMeyer/stlv) encoding with the numeric id from the above table as the type, and the public key as the value.

A *canonic binary yamf-signatory* uses the canonic binary encoding of the stlv.

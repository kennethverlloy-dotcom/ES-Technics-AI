# Overzicht Priva

Deze map bevat uitsluitend Priva-informatie. Priva is een kernspeler in gebouwbeheersystemen en wordt vaak toegepast in utiliteitsprojecten en zorgomgevingen.

Belangrijke platformen zijn **Priva Blue ID**, **Priva Top Control**, **TC Engineer**, **TC Select** en moderne cloud- of operatoromgevingen zoals **Building Operator**. Priva-systemen worden vaak geïntegreerd met BACnet- of Modbus-koppelingen en vragen een zorgvuldige engineeringsaanpak bij commissioning en service.

Aandachtspunten zijn correcte toewijzing van punten, duidelijke regelbeschrijving, back-up van controllers en het documenteren van parameterwijzigingen. Officiële documentatie verloopt via de relevante Priva-portalen en partnersites.

## Service Aandachtspunten
- **Back-ups:** Neem ALTIJD een back-up van de controller via TC Engineer voordat een parameterwijziging wordt doorgevoerd.
- **Modules:** Bij Blue ID modules, let op de LED-status. Een rode knipperende LED op een I/O module duidt vaak op een bus-communicatiefout of voedingsprobleem.
- **Forceer-status:** Controleer in TC Manager of er uitgangen manueel (geforceerd) overschreven staan (vaak aangeduid met een hand-icoon). Dit is een veelvoorkomende oorzaak van "onverklaarbaar" regelgedrag.

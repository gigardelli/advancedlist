FROM cr.sas.com/viya-4-x64_oci_linux_2-docker/sas-decisions-runtime-components:1.60.25-20240514.1715695392496 as base
FROM cr.sas.com/viya-4-x64_oci_linux_2-docker/sas-decisions-runtime-base:1.80.25-20240514.1715695377677
LABEL model container image
USER root
RUN chown sas:sas /modules
USER sas
ENV SAS_SCR_APP_PATH=/teste_scr_al1_2
COPY --chown=sas:sas unzipped/ /modules/
COPY --chown=sas:sas manifest/ /manifest/
COPY --from=base  /hiredis /
COPY --from=base  /hiredis /
ENV LD_LIBRARY_PATH=/opt/scr/viya/home/SASFoundation/utilities/bin:/opt/scr/viya/home/SASFoundation/sasexe

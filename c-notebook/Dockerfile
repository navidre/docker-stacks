# Distributed under the terms of the Modified BSD License.

FROM jupyter/minimal-notebook

LABEL maintainer="Navid Rezaei <navidres@gmail.com>"

USER root

USER $NB_USER

# C++ packages
RUN conda install --quiet --yes cling -c QuantStack -c conda-forge
RUN conda install --quiet --yes xeus-cling -c QuantStack -c conda-forge
RUN conda clean -tipsy && \
    fix-permissions $CONDA_DIR
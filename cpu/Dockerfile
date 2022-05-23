FROM ecpe4s/ubuntu20.04-spack
MAINTAINER John Jolly (john.jolly@utah.edu)

# Copying package.py only works this way because docker-compose allows
# us to set a different root directory for files. This way all the
# various container types can use one Spack package.py
COPY package.py /spack/var/spack/repos/builtin/packages/bricks/

RUN . /spack/share/spack/setup-env.sh && spack install bricks target=x86_64 && spack clean -a

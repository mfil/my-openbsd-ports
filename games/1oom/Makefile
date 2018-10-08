COMMENT=	Master Of Orion engine recreation

VERSION=	0.9
DISTNAME=	1oom-v${VERSION}
CATEGORIES=	games x11

HOMEPAGE=	https://kilgoretroutmaskreplicant.gitlab.io/plain-html/

# GPLv2+
PERMIT_PACKAGE_CDROM=	Yes

MASTER_SITES=	https://gitlab.com/KilgoreTroutMaskReplicant/1oom/-/archive/v${VERSION}/

WANTLIB=	SDL2 SDL2_mixer samplerate c

CONFIGURE_STYLE=	autoconf automake
AUTOCONF_VERSION=	2.69
AUTOMAKE_VERSION=	1.16
AUTOCONF=		autoreconf -fi
CONFIGURE_ARGS=		--disable-hwsdl1 --disable-hwalleg4

.include <bsd.port.mk>

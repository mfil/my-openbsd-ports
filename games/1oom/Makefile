# $OpenBSD$

COMMENT=	Master Of Orion engine recreation

VERSION=	1.0
PKGNAME=	1oom-${VERSION}
CATEGORIES=	games x11

HOMEPAGE=	https://kilgoretroutmaskreplicant.gitlab.io/plain-html/

# GPLv2+
PERMIT_PACKAGE_CDROM=	Yes

DISTNAME=	1oom-v${VERSION}
MASTER_SITES=	https://gitlab.com/KilgoreTroutMaskReplicant/1oom/-/archive/v${VERSION}/

WANTLIB=	SDL2 SDL2_mixer samplerate c

LIB_DEPENDS=	audio/libsamplerate \
		devel/sdl2 \
		devel/sdl2-mixer

CONFIGURE_STYLE=	autoconf automake
AUTOCONF_VERSION=	2.69
AUTOMAKE_VERSION=	1.16
AUTOCONF=		autoreconf -fi
CONFIGURE_ARGS=		--disable-hwsdl1 --disable-hwalleg4

post-install:
	/bin/ln -s ${TRUEPREFIX}/bin/1oom_classic_sdl2 ${PREFIX}/bin/1oom
	cd ${WRKBUILD}/doc/; make install-recursive
	/bin/mkdir -p ${PREFIX}/share/1oom
	${PREFIX}/bin/1oom_pbxmake ${PREFIX}/share/doc/1oom/pbxin_fixbugs.txt \
	    ${PREFIX}/share/1oom/fixbugs.pbx

.include <bsd.port.mk>
